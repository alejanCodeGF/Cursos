# C:

## Comentar en el codigo:

```
    "//" delante de la linea de codigo
    "/*" al inicio y "*/" al final del comentario
```

## Declaración de una variable/parametros:

```
    tipoDato nombreVariable = dato
```

## Condicionales:

```
    if (condición){codigo}
    elseif (condición){codigo}
    else{codigo}
```

## Loops:

```
    while (condición){codigo}
    for (int i = 0; "i < 10; i++") __(lo que hay entre "" es un ejemplo)__
    	{codigo}
```

## Funciones:

```
    tipoDatoADevolver nombreFuncion(parametros){codigo} (parametros tipo int a, char c, etc)
```

> Si no devuelve ningun dato poner 'void'

## Operadores lógicos:

```
    '&&' (and)
    '||' (or)
    '!'  (not)
```

## Importar modulos:

```
    #include <libreria>
```

## Manejo de excepciones:

```
    try
		{codigo con posibles bugs}
	catch...
		{codigo que hará si peta 'try'}
    finally:
		{codigo que hará siempre (p.e cerrar un archivo)}
```

> En el except poner el codigo de excepciones (si quieres unos en especifico, o globales, etc.)
> P.e. "(Exception e)",donde atrapa todas las excepciones globales y lo pone en la variable 'e'

## Otros:

```
Es obligatorio acabar con ";" en las sentencias
do-while (en python whiletrue-break)
Si vas a usar una funcion en el main, tiene que estar por encima (a no ser que escribas su contructor abajo y ya encima "tipodato nombrefuncion(parametros);")
```
