# HTML

`>` No se si hace falta decirlo, pero obviamente lo que este en el HTML, CSS y JS será publico, asi que no poner cosas privadas vaya (ni en comentarios)

## Links interesantes

[**{Link a un cheatsheet interactivo}**](https://htmlcheatsheet.com/)

## Comentar en el codigo

```
<!--COMENTARIO-->
```

## Teoria antes de empezar

```
Al archivo que quieras que arranque la web le pones el nombre de "index.html"
    > Es el que mostrará la web de primeras

Estructura:
[<etiqueta atributo="valor">contenido</etiqueta>]
    > Habrán algunos que no necesiten etiqueta de cierre, para esos
    [<etiqueta atributo="valor" />]
        > Algunos dicen que no le pongas el "/", para que quede mas limpio
            > Yo lo he hecho teniendo en cuenta el cierre, lo que veas

Display:
    block -> Completan la linea hasta el final del contenedor (h1, h2... p, etc.)
        > Por mas pequeño que sea el texto, no se puede poner nada mas a la derecha
    inline -> Ocupan el contenido unicamente (inputs, etc.)

Links:
1) Rutas locales (las que estan en nuestra carpeta)
    > "nombre_archivo.html" / "nombre_carpeta/nombre_archivo.html"
    > ../archivo -> ir a una carpeta anterior (si quieres 2 ../../etc)
2) Rutas externas (las de fuera de nuestra carpeta)
    > "https/www...."

> Bool (boleano) significa que no hace falta introducir ningun dato para activarlo
    > Se suele poner por nomenclatura de nombre el mismo atributo
        > (P.e: <ol reversed = "reversed">, o <video controls = "controls">)
        > Algunos dicen que lo pongas vacio (<ol reversed>, que se ve mas limpio)
```

## Especificar version del HTML

```
HTML5 -> <!DOCTYPE HTML>
HTML4 -> <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
XHTML1 ->
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```

`>` A partir de ahora, todo el codigo irá rodeado de `<html></html>`

`>` (Si está tabulado, es un atributo de esa etiqueta)

## `<head>`

`>` Aqui van los elementos que no se ven directamente en la web

```
<title> añadir titulo en la pestaña
<meta> añadir metadatos
<link> linkear algo (archivo css, icono, etc.)
```

### _Metadatos / link_

```
Metadatos -> Información, que describe datos (recursos)
<meta>
    charset -> Cambiar la codificación (poder poner tildes y eso)
        = "utf-8" -> El mas usado para los idiomas europeos
    name -> Crear una "carpeta" de datos con ese nombre
        ="keywords" -> Etiquetas para el SEO, separadas por comas
        ="description" -> Descripción de la pagina web (entre 70-140 char)
        ="autor" -> Nombre del autor de la web
        ="copyright" -> Poner el nombre de la empresa dueña de los derechos
            > (P.e: Facebook (meta) tiene instagram)
        ="robots" -> Hablar con el buscador
            > Si la web deberia ser indexada o no (que aparezca en el buscador)
                > content = "index" / "noindex"
            > Si deberia dar importancia en el SEO
            (Le dicen al buscador si debe explorar las páginas a las que llevan o no)
                > content = "follow" / "nofollow"
    content -> De ese name, poner los datos
        > (P.e: name="keywords" content="harina, pasteles, huevos, lacteos")

<link>
    rel -> Que es lo que linkamos
        ="icon" -> Icono de la pestaña
            > Importante que tenga formato .ico
        ="stylesheet" -> Archivo de estilo (css)
    type -> Que formato tiene
        ="image/png"
        ="text/css"
    href -> link donde esté ese archivo
```

```
Ejemplos:
<link rel="icon" type="image/png" href="Fotos/Logos/Logo_wep32x32trans.ico">
<link rel="stylesheet" type="text/css" href="style.css">
```

## `<body>`

`>` Todo los elementos que se ven

### _Textos_

```
<hi> -> Añadir titulos (y solo titulos)
    > i = 1,2,...,6 (1 titulo, 2 subtitulo, 3 subsubtitulo...)
    > Añadir un unico h1 (por el SEO)
<p> -> Paragrafo de texto
<hr /> -> Linea de separación
<br /> -> Salto de linea
<span> -> Aplicar estilos a un grupo de letras (CSS)
<a> -> Poner links
    href = "https://...", o puede ser de la misma web
        > Para mandar a una parte de la misma web:
            > Poner al elemento que queramos ir un "id"
            > href="#nombre_id"
    target = "_blank", abrir en otra pestaña
```

### _Multimedia_

```
<img /> -> poner una imagen
    > png, jpg o gif lo aceptan todos los navegadores
    src = "link" o "imagen" (si esta en la misma carpeta "imagen.png")
    width = ...
    height = ...
        > Si pones uno de los 2, se escala automaticamente
    alt -> Texto alternativo si no carga la imagen / contenido
        > VITAL para el SEO
    title -> Texto que sale cuando pasas el raton por encima de la imagen
<video /> -> Poner un video
    src = "link" o "video"
        > Debe ser formato video
    controls (bool)
        > Nos permite acceder a los controles del video
        > Lo define el navegador
        > Si no esta no hacemos nada vaya
<audio /> -> Poner un audio
    > Lo mismo que el video vaya
    > En formato video reproduce el audio
```

### _Formularios_

```
<form> -> Rodeando el form de la info que quieras enviar
    action = "/formulario.php" (Donde se enviará el formulario)
    method -> Enviar la info del formulario
        = "GET" (parametros en la URL (hay tope de información, se suele usar para navegadores))
        = "POST" (No hay limite de información, el mas usado)
        > Ningun metodo es seguro
<label /> -> Enfocar la atencion al input cuando se clicke el texto
    for -> id del input asociado
    > Es un poco una tonteria
    > (P.e: Pones el texto "email" al lado del input, y cuando clickes el texto (y no el input), puedes empezar a escribir)
<input /> -> Para introducir la info (texto, checkbox, etc.)
    id -> Valor unico del elemento
    name -> "key" del json al enviar el formulario
        > Muy importante para enviar los datos
        > (P.e:{"Nombre":"Alejandro", "Edad":"..."})
    value -> Valor por defecto
        > Se mantiene, no como el placeholder
    placeholder -> Texto de ayuda
        > Cuando vayas a escribir desaparece ese texto
    type
        = "text" (Por defecto) -> Introducir texto
        = "email" -> Solo permite enviar si tiene formato mail (aaa@bbb.ccc)
            > Mejor hacerlo por el backend, pueden inventarse el mail
        = "number" -> No permite escribir texto
            > Flecha arriba y abajo para sumar y restar numeros
        = "password" -> Cuando escriba salen los ***
        = "radio" -> De varias opciones poder elegir solo 1
        = "checkbox" -> De varias opciones poder elegir las que quieras
        = "range" -> Mover una flechita para selecionar un numero
            > Rollo lo de instagram, de poner un rango de si te gusta mas o menos
            min (numero minimo)
            max (numero maximo)
        = "date" -> Fecha
        = "time" -> Hora
        = "color" -> Seleccionar un color
<textarea> -> Muy parecido al input text, pero un poco diferente
    id...
    ...
    cols = "numero de columnas" (entiendo que char)
    row = "numero de filas"
    readonly (bool)
    > No se usa "value", como el input, para hacerlo poner el texto entre las etiquetas
<button> -> Un botón vaya
    > Se puede poner texto al botón, incluso una imagen (entre las etiquetas)
    type
        = "button" Para que el js haga cosas
        = "reset" Dejar los valores del form por defecto
        = "submit" Enviar los datos del form
```

### _Listas_

```
<ul> -> Lista no ordenada
<ol> -> Lista ordenada (1,2,3...)
    start -> Numero desde donde quieres empezar la lista
        > Los siguientes lo continuarán
    type -> Tipo de ordenación
        = "A" (A,B,C,D...)
        = "a" (a,b,c,d...)
        = "I" (I,II,III,IV...)
        = "i" (i,ii,iii,iv...)
    reversed (bool)
<li> -> Cada elemento de la lista irá rodeado de esta etiqueta

<dl> -> Lista de descripción
    > (Rollo elemento1-descripción1, elemento2-descripción2, etc.)
<dt> -> Cada elemento de la lista irá rodeado de esta etiqueta
<dd> -> Cada descripción del elemento de la lista irá rodeado de esta etiqueta

> Se pueden añadir listas dentro de listas
```

### _Tablas_

```
Las tablas se organiza por filas y elementos

<table> -> Rodeando la tabla
<tr> -> Table row, fila de la tabla
<td> -> Celdas
    > Elementos que ponemos dentro de las filas <tr>
    colspan = "num de columnas"
        > Juntar varias columnas para poner 1 elemento
    rowspan = "num de filas"
        > Juntar varias filas para poner 1 elemento
<th> -> Como td, pero para poner los apartados de la tabla (encabezado)
<caption> -> Comentario arriba de la tabla
    > (P.e: nombre de la tabla)

Para organizar la tabla usar estos 3 grupos
<thead> -> Sección de encabezado
    > (P.e: nombre, edad... (ponerlo con <th>))
<tbody> -> Elementos de la tabla (datos)
<tfoot> -> Representar información resumen
    > (P.e: mediana, valor maximo, etc.)
```

### _Organizar la web_

```
Como cajas con otros elementos dentro, sirve para ordenar la web
    > Separar y agrupar contenido para organizar mejor

<div> -> El basico, contenedor normal generico
<header> -> Contenedor de arriba de la web
    > Siempre se mantiene igual mientras navegas por otros enlaces de la web
<nav> -> Navegador (buscador, cuenta, logo, etc)
    > Normalmente dentro del header
<main> -> Contenido principal de la web
    > (P.e: Donde se verán las noticias, si es un periodico)
<article> -> Separar lo del main por articles
    > (P.e: Las noticias individuales)
<section> -> Separar el contenido del article
    > No se si es lo mismo que <figure>
        > Hay sitios que lo veo con esa etiqueta nose
<aside> -> Informacion relacionada
<footer> -> Pie de pagina (copyright, contactanos, links relacionados, etc.)
```

### _Enlazar JavaScript_

```
Normalmente va al final del <body>, mas visible

<script> -> Para añadir el archivo de JS
    src = "archivo.js"
```
