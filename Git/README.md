# Git:

[Descarga Git](https://git-scm.com)

> HEAD -> Donde estamos nosotros
> main / master -> Final de nuestra rama

## Comandos

### Configurar git

```
$ git config --global user.name "[name]" -> Establecer nombre |
$ git config --global user.email "[email]" -> Establecer mail | [user]
$ git config --global alias.nombrealias "comandoalias" -> establecer un nombre a un comando
```

> La cuenta es la que se verá cuando hagas los commits
> Ejemplo de alias: git config --global alias.tree "log --graph --decorate --all --oneline" (luego lo llamas con "git tree")

### Crear repositorio

```
$ git init [project-name] -> Inizializar git en la carpeta
$ git clone [url] -> Clonar repositorio
$ git remote add origin "URL" -> Añadir de origen el repositorio a la carpeta (hacer init antes)
```

> Se mantienen los commits y toda la info del historial

### Sincronizar cambios

```
$ git fetch ([bookmark]) -> Descarga el historial del repositorio (sin descargar los cambios)
$ git merge ([bookmark]/[branch]) -> Combina la rama commit con la rama local (comprobar irregularidades)
$ git pull -> Igualar los commits del servidor con los del local (todo)
```

> Si no lo haces y has editado algo, puede haber errores

### Modificación ficheros

```
$ git add [file] -> Añadir 'file', para luego hacer commit (poniendo * se añaden todos)
$ gir rm [file] -> Eliminar archivo, y git lo tendrá en cuenta
$ git rm --cached [file] -> Quitar archivo añadido en el add
$ git mv [file_name][new_name] -> Cambiar el nombre de un fichero, y git lo tendrá en cuenta
$ git commit -m “[descriptive message]” -> Crea version con los archivos, pudiendo poner un mensaje
$ git push -> Subir los commit al servidor (web, nube, etc)
$ git checkout [file] -> Devolver el fichero a como estaba en el commit
$ git reset [file] ->
```

### Modificación de versiones

```
$ git checkout [commit] -> Volver a una version (con todo lo que tenias), sin perder el historial (HEAD)
$ git reset [commit] -> deshace los commits posteriores, preservandolos en local
$ git reset --hard [commit] -> deshace los commits posteriores, y los elimina (funciona hacia atras como hacia delante) (HEAD y main)
```

> "Diferencia de reset --soft, --mixed y --hard" [(link)](https://www.howtogeek.com/wp-content/uploads/csit/2021/07/f5026f58.png?trim=1,1&bg-color=000&pad=1,1)
> Para recuperar con "git reset --hard", hacer "git reflog", y hacer otro "git reset --hard" con el hash que antes era el main

### Etiquetas

```
$ git tag nombre_tag -> Pone una etiqueta en el hash que estes
$ git tag -> Ver tus tags
```

> Se puede mover de un commit a otro usando el tag (git checkout tags/nombre_tag)

### Información del git

```
$ git status -> Información de que archivos estan o no agregados
$ git diff -> Mostrar las diferencias de los archivos actuales respecto el ultimo commit
$ git diff --staged -> Mostrar las diferencias de los archivos añadidos al add respecto el ultimo commit
$ git diff [branch1][branch2] -> Muestra las diferencias entre 2 ramas (entiendo que pueden ser 2 commits por ejemplo)
$ git log -> Información de los commits realizados
$ git log --follow [file] -> Historial del archivo
$ git reflog -> Historial completo de interaciones de nuestro git
$ git show [commit] -> Muestra info detallada del commit (hash, autor y fecha, mensaje commit, cambios, diferencias de los archivos)
```

### Guardar Fragmentos

```
$ git stash -> Crear un "commit" temporal, una version inacabada
$ git stash pop -> Volver al stash anterior
$ git stash list -> Lista de los stashes
$ git stash drop -> Eliminar el stash mas reciente
$ git stash clear -> Eliminar todos los stashes
```

> Se guarda la version en local unicamente
> Se suele usar cuando vas a cambiar a otra rama sin tener 100% el codigo bien

### Ramas

> Trabajos temporales, se mezclarán con la rama principal y se borrarán

```
$ git branch -> Enumera todas las ramas actuales
$ git branch [branch-name] -> Crea una nueva rama
$ git switch -c [branch-name] -> Cambia a la rama especificada y actualiza el directorio activo
$ git merge [branch-name] -> Mergear la rama en la que estes con otra
$ git diff [branch-name] -> Mirar las diferencias que hay con otra rama
$ git branch -d [branch-name] -> Borra la rama
```

> Mergear ya lo he explicado en "sincronizar cambios"
> Al hacer merge, sincroniza la rama que quieres mergear (branch-name) con la rama en la que estas

### Los innombrables

> Usarlos solo si los entiendes bien, y los necesitas (simplemente tenerlo presente)

```
$ git cherry-pick [commit] -> Irnos a un commit concreto (ya borrado), y traerlo a la rama actual
    --continue -> Vamos haciendo poco a poco los que dan error
    --abort -> Parar el proceso, y nada a pasado
$ git rebase [rama] -> Traernos una rama hasta un punto en concreto (modificando el historial de los commits)
    --continue -> Vamos haciendo poco a poco los que dan error
    --abort -> Parar el proceso, y nada a pasado
```

## Ignorar archivos que no quieras añadir (add)

```
- Crear archivo llamado ".gitignore"
- Dentro, añadir los archivos temporales de esta forma: " **nombre_archivo "
```

> P.e.:
> **/.DS_Store (en C)
> **pycache (en python)
> (Y ya no te saldá cuando hagas add)

## Git workflows

> Flujos de trabajo con Git, para trabajar en conjunto de forma mas organizada

### Gitflow

[Video explicativo de WonCode](https://www.youtube.com/watch?v=atYIzPIeeQk)
[Gitflow](https://www.atlassian.com/es/git/tutorials/comparing-workflows/gitflow-workflow#:~:text=%C2%BFQu%C3%A9%20es%20Gitflow%3F,vez%20y%20quien%20lo%20populariz%C3%B3)

### Github flow

[Video explicativo de CodelyTV](https://www.youtube.com/watch?v=2Xagp86uOuI)
[Github Flow](https://docs.github.com/en/get-started/getting-started-with-git/git-workflows)

### Trunk-Based Development

[Video explicativo de CodelyTV](https://www.youtube.com/watch?v=-73RVTQxUhs)
[Trunk-Based Development](https://trunkbaseddevelopment.com/)

### Ship / Show / Ask

[Video explicativo de Midudev](https://www.youtube.com/watch?v=3FssKkNqUHE)
[Ship Show Ask](https://martinfowler.com/articles/ship-show-ask.html)
