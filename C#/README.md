# C#

**Basico de C# para empezar a programar**

> No está acabado. Faltan muchos apartados. A medida que tenga tiempo libre se irá completando

## Comentar en el codigo

```
'//' delante de la linea de comentario
' /* ' al inicio y ' */ ' al final del comentario
```

## Buenas practicas

```
> No dejar lineas vacias
> Bloque dentro de otro separado por tab
> Nombre variables y metodos:
> No comenzar por "_"
> No diferenciar variables por una letra (edad, Edad, edaD... mal)
> Comenzar por minuscula, y si tiene varias palabras separarlas por mayuscula (miVariable)
> No usar notación húngara (lista -> lcompra, etc. mal)
> Si es una variable constante, ponerlo en mayusculas
> Al programar hacerlo en pequeñas partes y luego juntarlas
> Poner "private" para encapsular (no hace falta, pero queda mas claro)
> Si necesitamos modificar una cte/variable, lo haremos mediante metodos
> (metodos de acceso), no es buena practica poner "public" en la variable
> Los identificadores (variables, ctes, metodos)
|Coming soon|
```

## Tipo de datos

|Coming soon|

### Por valor

```
Los maneja el ordenador (procesados) y se almacena en una variable
```

#### Primitivos

```

```

### Por referencia

```
Almacenamos una dirección

```

## Operadores aritmeticos

```
(+, -, *, /, **, //, %)
... (basico)
** -> Elevado (2 ** 3 -> 8)
// -> División entera entre 2 numeros (10 // 3 -> 3)
% -> Residuo de la división (10 % 3 -> 1)
++ -> Incremento (4++ == 5)
-- -> Decremento (4-- == 3)
+= n -> Incremento n veces (4 += 3 == 7)
-= n -> Decremento n veces (4 -= 3 == 1)
```

## Declaración de variable

```
tipo_dato nombre_variable - Declarar variable
nombre_variable = dato - Inicializar variable
tipo_dato nombre_variable = dato - Declarar e iniciar en 1 linea
```

```
> Si pones un dato que no sea compatible dará error
> Es posible declarar varias, y inicializar varias simultaniamente
    p.e. int edad1, edad2, edad3;
         edad1 = edad2 = edad3 = 27; (Todos tendrán un valor de 27)
```

## Funciones de consola

```
"using System" (libreria) (si no lo pones, poner system. antes (system.console...))
console.writeline() -> Poner dentro lo que quieras imprimir
```

## Convertir a otros tipos de dato

### Conversion explicita (Casting)

```

```

### Conversion implicita

```

```

### Type conversion

```

```

## Strings

### Metodos str

```
|Coming soon|
```

### Interpolación de strings

```
Poner otro tipo de datos en un string (variables, etc.)
$"Texto{variables}texto"
> c.w($"Tengo {edad} años")
```

## Funcionamiento de C#

```
Aqui iran excepciones importantes:
> El codigo va de izquierda a derecha, lo que quiere decir que si hay incremento, lo hará despues de leer el dato
    p.e. cw("Tengo " + edad++ + " años") (edad == 12 p.e.)
    tengo 12 años, edad == 13 (imprime 12, y luego lo suma)
Para evitarlo, ponerlo delante (++edad), y ahora suma, y luego lee (funciona bien)
```
