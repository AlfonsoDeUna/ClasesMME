# DEL MODELO DE VON NEUMANN AL INFINITO PASANDO POR EL ANÁLISIS DE MALWARE 

## ENSAMBLADOR EN LINUX PARA CONOCER EL LENGUAJE MÁQUINA
https://riptutorial.com/es/assembly

## DEL LIBRO DE TEXTO
TEMA 2 PRIMERA PARTE

## TEORÍA DEL MODELO DE VON NEUMANN
http://docencia.ac.upc.edu/eines/MR/DOCUMENTOS/Transparencies/slides_CPU.pdf

## OTROS SIMULADORER

### MAKINITO
* https://fvarrui.github.io/Makinito/
![Alt text](https://fvarrui.github.io/Makinito/images/interfaz.png?raw=true "MAKINITO")

## Ejercicios que se desarrollan con un simulador de Von Neumann ALTERVISTA

[Enlace simulador Von Neumann] http://vnsimulator.altervista.org/

### Nemónicos que están disponibles en este simulador
* LOD
* STO
* ADD
* SUB
* MUL
* DIV
* JMP
* JMZ


### Ejercicio 1: 
- [x] Crea una pequeña rutina en la que compare dos número almacenados en dos registros del micro en el **registro X** contiene un número
      y en el **registro Y** contiene otro número. *Si X>Y entonces el **registro Z** = 1 sino **registro Z** = 0*
      
      ```
            // X > Y ? Z
            LOD X
            JMZ 11
            SUB #1
            STO X
            LOD Y
            JMZ 15
            SUB #1
            STO Y
            JMP 1
            // X < Y
            LOD #0
            STO Z
            HLT
            // X > Y
            LOD #1
            STO Z
            HLT
      ```

### Ejercicio 2: 
- [ ] Crea una pequeña rutina en la que realice 2^X siendo el **registro X** el exponente.
  el **registro Y** contiene el resultado.
