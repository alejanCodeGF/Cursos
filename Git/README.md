# Git:

## Comandos

```
git clone [url] -> clonar un repositorio
git status -> información de que archivos estan o no agregados
git add [file] -> añadir file (si pones * se añaden todos)
git rm [file] -> quitar archivo añadido con el add
git commit -m “[descriptive message]” -> crea version con los rchivos, y puedes poner un mensaje
git log -> información de los commits realizados
git push -> subir los commit al servidor (web, nube, etc)
git pull -> igualar los commits del servidor con los del local (si no lo haces y has editado algo, puede haber errores)
```

## Ignorar archivos que no quieras añadir (add)

```
.gitignore -> " **nombre_archivo "
```

> p.e:
> nombre_archivo == .gitignore
> **/.DS_Store (en C)
> **pycache (en python)
> (Y ya no te saldá cuando hagas add)
