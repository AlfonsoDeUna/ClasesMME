## Gestión de discos duros a través de PowerShell
***

### Obtener información del disco

```
> Get-Disk

```


### Formatear el disco
A partir de Get-Disk obtenemos el identificador del disco duro que queremos gestionar. Cambia el 0 por el número de tu disco


```
> Get-Disk 0 | Clear-Disk-RemoveData
```

El disco desaparecerá y ahora lo inicializamos

```
> Initialize-Disk 0
```

###Creamos una nueva partición

```
> New-Partition -DiskNumber 0 -UseMaximumSize| Format-Volume -FileSystem NTFS -NewFileSystemLabel Archive
```
*  **DiskNumber:** El disco que queremos formatear.
*  **UseMaximumSize:** Queremos que afecte completamente al disco completo.

* **FyleSystem**: Seleccionamos el tipo de sistema de ficheros que queremos.
* **NewFileSystemLabel:** Le damos un nombre de volumen al disco

Y por último necesitamos realizar esta acción y veremos el disco duro en el explorador
```
> Get-Partition - DiskNumber 0 | Set-Partition -newDriveLetter D:
```

### Obtener información sobre ordenadores remotos, ocupación del disco

 ```
 Get-WMIobject win32_LogicalDisk -ComputerName $computers -filter "DriveType=3" |
                Select-Object SystemName, DeviceID, VolumeName,
                @{Name="Size(GB)"; Expression={"{0:N1}" -f($_.size/1gb)}},
                @{Name="FreeSpace(GB)"; Expression={"{0:N1}" -f($_.freespace/1gb)}},
                @{Name="% FreeSpace(GB)"; Expression={"{0:N2}%" -f(($_.freespace/$_.size)*100)}},
                @{Name="Date"; Expression={$(Get-Date -format 'g')}} 
 ```               
 
 Para más información: https://www.signalwarrant.com/remotely-retrieve-disk-space-size-freespace-freespace-powershell/
 
