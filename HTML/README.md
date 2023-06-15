# HTML

[Link a un cheatsheet interactivo](https://htmlcheatsheet.com/)
No se si hace falta que lo diga, pero obviamente todo lo que este escrito en el HTML, CSS y JS será publico, aunque esté comentado. Asi que no poner cosas privadas vaya

## Comentar en el codigo:

```
<!--COMENTARIO-->
```

## Especificar version del HTML

```
HTML5  -> <!DOCTYPE HTML>
HTML4  -> <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
XHTML1 -> <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```

<br>

> A partir de ahora, todo el codigo irá rodeado de `<html></html>`
> Si está tabulado, es un atributo de esa etiqueta

## `<head>`

> Aqui van los elementos que no se ven directamente en la web

```
<title> añadir titulo en la pestaña
<meta> añadir metadatos
<link> añadir archivo css
```

> Ejemplo css`<link rel="stylesheet" href="style.css">`

## `<body>`

> Todo los elementos que se ven

### _Textos_

```
<hi> Añadir titulos (y solo titulos)
i = 1,2,...,6 (1 titulo, 2 subtitulo, 3 subsubtitulo...)
<p> Paragrafo de texto
<hr /> Linea de separación
<br /> Salto de linea
<span> Aplicar estilos a un grupo de letras (CSS)
<a> Poner links
    href = "https://...", o puede ser de la misma web
    target = "_blank", abrir en otra pestaña
<img /> (png, jpg o gif lo aceptan todos los navegadores)
    src = "link" o "imagen" (si esta en la misma carpeta "imagen.png")
    width = ... |
    height = ...| Si pones uno de los 2, se escala automaticamente
```

### _Formularios_

```
<form> (rodeando el form de lo que quieras enviar)
    action = "/formulario.php" (Donde se enviará el formulario)
    method (Ningun metodo es seguro)
        = "GET" (parametros en la URL (hay tope de información, se suele usar para navegadores))
        = "POST" (No hay limite de información, el mas usado)
<label /> (...)
<input /> (Para introducir la info (texto, checkbox, etc.))
    id = "id_1" (valor unico del elemento)
    name = "key" (key del json al enviar el formulario
        (p.e.{"Nombre":"Alejandro", "Edad":"..."})) (muy importante)
    value = "valor por defecto" (se mantiene, no como el placeholder)
    placeholder = "ayuda para el user" (texto de ayuda, cuando vayas a escribir desaparece)
    type
        = "text" (el predeterminado, introducir texto)
        = "email"
        = "password" (cuando escriba salen los ***)
        = "radio" (de varias opciones poder elegir solo 1)
        = "checkbox" (de varias opciones poder elegir las que quieras)
        ...
<textarea> (muy parecido al input text, pero mas grande)
    id...
    ...
    cols = "numero de columnas" (entiendo que char)
    row = "numero de filas"
    (no usa value como el input, para hacerlo poner el texto entre las etiquetas)
<button> (se puede poner texto al botón, incluso una imagen (entre las etiquetas))
    type
        = "button" Para que el js haga cosas
        = "reset" Dejar los valores del form por defecto
        = "submit" Enviar los datos del form
```

### _Listas_

```
<ul> lista no ordenada
<ol> lista ordenada (1,2,3...)
    start (numero desde donde quieres empezar la lista (los siguientes lo continuarán))
    type (tipo de ordenación)
        = "A" (A,B,C,D...)
        = "a" (a,b,c,d...)
        = "I" (I,II,III,IV...)
        = "i" (i,ii,iii,iv...)
    reversed (booleano)
<li> (cada elemento de la lista irá rodeado de esta etiqueta)

<dl> lista de descripción (elemento1-descripción1, etc.)
<dt> (cada elemento de la lista irá rodeado de esta etiqueta)
<dd> (cada descripción del elemento de la lista irá rodeado de esta etiqueta)
```

> Booleano significa que no hace falta introducir ningun dato
> Se suele poner por nomenclatura de nombre el mismo atributo (`<ol reversed = "reversed">`)
> Se pueden añadir listas dentro de listas

### _Tablas_

```
Las tablas se organiza por filas y elementos
<table> (rodeando la tabla)
<tr> table row, fila de la tabla
<td> celdas (elementos que ponemos dentro de las filas <tr>)
    colspan = "num de columnas" (juntar varias columnas para poner 1 elemento)
    rowspan = "num de filas" (juntar varias filar para poner 1 elemento)
<th> como td, pero para poner los apartados de la tabla (encabezado)
<caption> comentario arriba de la tabla (p.e. nombre de la tabla)
Para organizar la tabla usar estos 3 grupos
<thead> sección de encabezado (nombre, edad... (ponerlo con <th>))
<tbody> elementos de la tabla (datos)
<tfoot> representar información resumen (media, valor maximo, etc.)
```

### _Enlazar JavaScript_

```
<script> (para añadir el archivo de JS)
    src = "archivo.js"
```
