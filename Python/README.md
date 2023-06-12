# Python

En este curso habrá un **cheatsheet** de lo mas importante de python (loops, etc.)

## Comentar en el codigo:

```
'#' delante de la linea de comentario
' """ ' al inicio y al final del comentario (3 comillas dobles)
```

## Declaración de una variable/parametros:

```
nombre_variable = dato (son dinamicos, se pueden cambiar de tipo de dato)
```

> Aunque sea dinamico, se puede "declarar" el tipo de una variable **func(numero : int)**
> Sirve para dar info a los desarrolladores, o para frameworks que no permiten el dinamismo de python

## Condicionales:

```
    if condición:
    	codigo
    elif condición:
    	codigo
    else:
    	codigo
```

## Loops:

```
    while condición:
    	codigo
    for i in iterable:
    	codigo
```

> Si no le vas a dar uso a **'i'** puedes poner **'_'**, haciendola anonima

## Funciones:

```
    def nombre_funcion(parametros):
    	codigo
```

## Operadores lógicos:

```
    'and'
    'or'
    'not'
```

## Importar modulos:

```
    import libreria/fichero
    from libreria/fichero import func_especifica1, func_especifica2...
    from libreria/fichero import func_especifica1 as func1 (renombra la funcion)
```

## Manejo de excepciones:

```
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

## Otros:

```
whiletrue-break (do-while en C)
```
