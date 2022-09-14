# SOLUCIÓN A LOS RETOS

## 1.1 Display number of dots for a given number of cards

```python

print ("1")
print ("2")
print ("4")   
print ("8")
print ("16")

```

##  1.2 Display Binary Numbers (using a variable)

Solución sencilla:

```python

number_of_dots = 0
number_of_dots += 1
print (number_of_dots)
number_of_dots = number_of_dots*2
print (number_of_dots)
number_of_dots = number_of_dots*2
print (number_of_dots)   
number_of_dots = number_of_dots*2
print (number_of_dots)
number_of_dots = number_of_dots*2
print (number_of_dots)

```

Solución con bucles

## 1.3 Display Binary Numbers (using variables as an operator)


```python

number_of_dots = 1
print (number_of_dots)
number_of_dots = number_of_dots * 2
print (number_of_dots)
number_of_dots = number_of_dots * 2
print (number_of_dots)
number_of_dots = number_of_dots * 2
print (number_of_dots)
number_of_dots = number_of_dots * 2
print (number_of_dots)

```

## 1.4 Display Binary Numbers (using a variable, operator and a repeat loop)


```python

number_of_dots = 1
while number_of_dots <= 16:
    print (number_of_dots)
    number_of_dots = number_of_dots * 2
    
```

## 1.5 Display number of dots for a given number of cards

```python 

number_of_cards = input()
number_of_cards = int(number_of_cards)
num = 1
num_of_dots = 1
while num <= number_of_cards:
    print (num_of_dots)
    num_of_dots = num_of_dots * 2
    num = num + 1

```
