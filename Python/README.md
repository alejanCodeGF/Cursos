# Cheatsheet de Python B-)

## Comentar código

```
'# ...comentario...' - Solo una única línea de texto
' """ ...comentario... """ ' - Varias lineas de texto
```

## Tipos de dato

- int (Enteros)
- float (Decimales)
    - Incluso 227.0 se considera float
- string (Cadena de caracteres)
    - Comillas simples o comillas dobles
- bool (True (o 1) / False (o 0))
- complex (Numeros complejos)

- list (Lista)
- tupple (Tupla)
- dict (Diccionario)
- set (Colección de datos única, no ordenada)

## Convertir a otros tipos

```
int(variable), float(variable), etc.
```

## Variables (snake_case)

```
nombre_variable = dato

Comportamiento dinámico (puedes cambiar el tipo de dato)
```

> Aunque sea dinamico, se puede "declarar" el tipo de una variable func(numero : int). Sirve para dar info a los desarrolladores, o para frameworks que no permiten el dinamismo de python

## Consola

### Escribir en consola

```
print(texto/s, end=final_texto)
    > texto = Lo que se quiere imprimir (puede ser cualquier tipo de dato)
        > Se pueden poner varios textos separados por comas, y lo imprimirá con un espacio entre textos
    > final_texto = Una vez imprime el print, le añade el "end" (De base es "/n", new line)
```

### Input desde consola

```
variable = input(texto_print) (la variable es para almacenar el input, pero no es obligatorio)
    > Escribirá el texto_print en consola, y pedirá un input al usuario
    > IMPORTANTE, el input siempre será de tipo texto, transformar si es necesario
```
## Operadores

```
Aritmeticos:
+ (suma), - (resta), * (multiplicación), / (división), ** (elevar), // (división sin decimales [D]), % (residuo [R])

Si puedes opera entre mismos tipos, pero hay excepciones:
> int y float siempre dará float
> Se puede hacer string*int -> 'stringstring...' "int" numero de veces
> String solo se puede sumar con string (concatenar strings)
> Si dividimos (aunque sean 2 int y de int) será float siempre (10 / 2 == 5.0)

Lógicos:
'and' ("a" y "b")
'or' ("a" o "b")
'not' (negación)

De comparación:
x == y "igual a"
x <= y "menor que"
x >= y "mayor que"
x != y "no igual a"/"diferente de"

Ejemplos curiosos:
> 3 <= 1: False
> abc > abd: a>a? igual -> b>b? igual -> c>d? NO -> False
> 7.0 == 7: True
> False and True or True: False and True? False -> False or True? True -> True
    > Es decir: ((False and True) or True) (Con los parentesis)

De asignación:
variable[operator]= valor
    > x += 6 <==> x = x + 6
    > (Y con los operadores +, -, *, /...)
```

## Control de flujo

### if-else

```
if condición:
    codigo
elif condición2:
    codigo2
else:
    codigo alterno
```

### for/while loops

```
while condición:
    codigo
for i in iterador:
    codigo

break -> Salir automáticamente del bucle sin finalizar
range(n) -> Función que crea una colección con el parametro que le demos: 0, 1, ... n-1
    > Si necesitas mas especifico: range(start, stop, step) (default start=0, step=1)
        > P.e: range(10, 0, -1) -> i: 10, 9, 8..., 2, 1
        > P.e: range(-10, 1, 2) -> i: -10, -8, -6..., -2, 0
```

## Colecciones de datos

### Listas

```
Colección ordenada por posición
lista = [dato0, dato1, dato2]

Consultar dato:
lista[0] - dato0

Modificar lista:
lista[0] = cambio_dato - [cambio_dato, dato1, dato2]

Otros:
Si el indice es negativo, consulta la lista al revés
    > lista[-1] consultará el ultimo dato, -2 el penultimo, etc.
Para copiar una lista no vale con copia_lista = lista (Copiará la referencia, si editamos uno editamos el otro (son el mismo))
    > copia_lista = lista[:]
    > copia_lista = lista.copy()
len(lista) -> Numero de elementos (len == indice mas grande + 1)
x_valor in lista: True / False - Saber si x valor está en la lista o no
```

#### Metodos

```
lista.append(dato) - Añadir un dato al final de la lista
lista.pop() - Elimina el último elemento, y hace return del valor
```

### Tuplas

```
Muy parecido a las listas

Colección ordenada pero inmutable
tupla = (dato0, dato1, dato2)

Consultar dato:
tupla[0] - dato0

NO es editable
tupla[0] = cambio_dato - ERROR

Otros:
var1, var2, var3 = (dato0, dato1, dato2) - Declarar varias variables con una tupla con varios valores
```

### Strings

#### Metodos

```
Metodos que EDITAN el string
string.upper() - Mayus
string.lower() - Minus
string.capitalize() - 1er char en mayus, las demás en minus
string.count("mi_str") - Cuenta el numero de veces que se repite "mi_str" en "string"
```

#### Variables dentro de strings (F strings)

```
f"...{variable/dato no string}..."
    > P.e: final_string = f"Hello {name}, I'm {6+8} years old" - "Hello Alejan, I'm 14 years old"

Formas alternativas:
final_string = "Hello {}, I'm {} years old".format(name, 6+8)
final_string = "Hello %s, I'm %d years old"%(name, 6+8) (Como en "C", s = string, d = numero (entre otros muchos))
```

#### Expresiones regulares

```
import re

|Coming soon|
```

### Similitudes entre listas, tuplas y strings

```
Los strings pueden ser tratados como listas de caracteres ("hola" -> string[0] = "h")
Por eso comparten algunos comportamientos con las tuplas y las listas
```

#### for/while loops

```
for i in lista: // i: dato0, dato1, etc.

range(len(lista)) -> Recorre todos los indices de la lista
    for i in range(len(lista)): - i: 0, 1, ..., len(lista)-1
enumerate(lista) -> Tupla para iterar por indice y valor
    > for i, element in enumerate(lista): - i: 0,1,... / element: dato0, dato1...
```

#### Slice operator

```
Cortar una colección

sliced = lista[start:stop:step] (como el range)

lista[::-1] -> Escribe la misma lista, pero al revés
```

### Sets

```
Colección unica y desordenada (sin elementos repetidos y sin orden)

Varias formas de declararlo:
mi_set = set() - Declarar un set vacio (set() != {}, ya que eso es un diccionario vacio, no set)
mi_set = {valor1, valor2, valor3} - Declarar set con varios valores (Si hay algun valor repetido lo eliminará)

valor in mi_set: True / False
    > Mejor que en listas ya que es MUCHO mas rapido

No se pueden añadir tipos de datos mas complejos (set, listas, o diccionarios y creo que objetos tampoco)
    > Pero por ejemplo tuplas si, nose
```

#### Metodos

```
mi_set.add(elemento) - Añadir elemento sin ningun orden (Un unico argumento)
mi_set.remove(elemento)
mi_set.union(mi_set2) - Hace return de todos los valores de los 2 sets
mi_set.intersection(mi_set2) - Hace return de unicamente los valores que estén en ambos sets
```

### Diccionarios

```
Colección de pares llave-dato
diccionario = {key : value} - El value puede ser cualquier valor (incluso list, etc.), pero la key no

Crear key-value / Editar value si la key ya existe:
diccionario[key] = value

Consultar dato dada una key:
diccionario[key] - value

Otros:
key in diccionario - True / False
del diccionario[key] - Elimina la key y el valor asociado
```

#### Metodos
```
diccionario.values() - Todos los valores del diccionario en formato dict_values
    > Para pasarlo a lista o a algo mas manejable -> list(diccionario.values())
diccionario.keys() - Todas las keys del diccionario en formato dict_keys
    > x2
diccionario.items() - Tupla con todos los key-value del diccionario
```
#### for/while loops

```
for key in diccionario: // key: key1, key2...
    > Haciendo "in diccionario" solo imprime las keys
for key, value in diccionario.items(): // key: key1, key2... / value: value1, value2...
```

## Funciones

```
Crear función
def nombre_funcion(parametros):
    codigo

Llamar a función
nombre_funcion(...)

return -> Lo que devolverá la función. Una vez lee el "return" sale de esta
```

### Lamda (Python)

|Coming soon|

### Funciones que usan funciones

|Coming soon|

## Clases y objetos

|Coming soon|

## Importar modulos

```
import libreria/fichero
from libreria/fichero import func_especifica1, func_especifica2...
from libreria/fichero import func_especifica1 as func1 (renombra la función)
```

## Archivos externos

|Coming soon|

### .txt

### .json

### .csv

## Excepciones y errores

```
Crear excepciones:
raise mi_excepcion("texto a poner en la excepción")
    > mi_excepcion puede ser "Exception", "FileExistError", etc. Lo que quieras

Evitar excepciones:
try:
    codigo con posibles bugs
except...:
    codigo que hará si peta 'try'
else:
    codigo que hará si no peta 'try'
finally:
    codigo que hará siempre (p.e cerrar un archivo)
```

> En el except poner el codigo de excepciones (si quieres unos en especifico, o globales, etc.)
    > Si pones: except mi_excepcion as e: -> print(e) te imprimirá el error
        > Hay una jerarquia de excepciones. Si quieres captar todas ponle "Exception"

## Otras cosas generales

|Coming soon|

### Modulos generales importantes

#### datetime

#### pandas

#### math