# Practice with Git and Github

### Globals

|Command|Description|
|-------|-----------|
|`git config --global user.name <name>`|Configurar globalmente el nombre de usuario.|
|`git config --global user.email <email>`|Configurar globalmente el correo electrónico.|

### Commonds

|Command|Description|
|-------|-----------|
|`git init`|Iniciar git en un nuevo proyecto.|
|`git branch <branch_name>`|Crear nueva rama.|
|`git checkout <branch>`|Cambiar de rama.|
|`git status`|Obtener el estado de los archivos en git.|
|`git add <.\|--all\|-A>`|Agregar todos los archivos al stage.|
|`git commit -m <message>`|Agregar un nuevo `commit`|
|`git push <origin\|remote> <branch\|master>`|Subir cambios|

### Status

|Command|Description|
|-------|-----------|
|`git status`|Obtener el estado de los archivos en git.|
|`git status -s`|Obtener el estado de los archivos en git, omitiendo datos innecesarios.|
|`git status -s -b`|Obtener el estado de los archivos en git, omitiendo datos innecesarios, incluyendo los nombres de las ramas.|

### Add 

|Command|Description|
|-------|-----------|
|`git add <.\|--all\|-A>`|Agregar todos los archivos al stage.|
|`git add <*.extension\|folder/*.extension>`|Agregar todos los archivos, de una extension específica, al stage.|
|`git add <folder/>`|Agregar todos los archivos, de una carpeta específica, al stage.|
|`git add <file>`|Agregar archivo específico al stage.|
|`git add -u`|Agregar todos los archivos actualizados al stage.|

### Commit

|Command|Description|
|-------|-----------|
|`git commit -m <message>`|Agregar un nuevo `commit`|
|`git commit -am <message>`|Agregar un nuevo `commit` agregando al `stage` todos los cambios.|
|`git commit --amend -m "<New message>"`|Cambiar el mensaje del ultimo `commit`.|

### Reset 

|Command|Description|
|-------|-----------|
|`git reset <.\|--all\|-A>`|Quitar todos los archivos del stage.|
|`git reset <*.extension\|folder/*.extension>`|Quitar todos los archivos, de una extension específica, del stage.|
|`git reset <folder/>`|Quitar todos los archivos, de una carpeta específica, del stage.|
|`git reset <file>`|Quitar archivo específico del stage.|
|`git reset HEAD <File>`|Quitar archivo del `stage`.|
|`git reset --soft HEAD^`|Deshacer el ultimo `commit` sin eliminar los cambios, dejando los cambios sin eliminar en el `stage`.|
|`git reset --mixed <hash>`|Deshacer todos los `commits` hasta llegar al `commit` con `hash` indicado, conservando los cambios y los archivos de los `commits` eliminados.|
|`git reset --hard <hash>`|Deshacer todos los `commits` hasta llegar al `commit` con `hash` indicado, borrando todos los cambios de los `commit` eliminados.|
|`git reflog`|Obtener el registro de todos los movimientos que se han hecho en el respositorio, con este comando se puede recuperar el `hash` de `commits` eliminados.|


### Diff

|Command|Description|
|-------|-----------|
|`git diff`|Lista las diferencias respecto al ultimo `commit`.|
|`git diff --stage`|Lista las diferencias del `stage` respecto al ultimo `commit`.|

### Checkout

|Command|Description|
|-------|-----------|
|`git checkout -- <.>`|Establecer el proyecto con el ultimo `commit`|
|`git checkout -- <File>`|Recuperar un archivo desde el ultimo `commit`.|

### Branch
|Command|Description|
|-------|-----------|
|`git branch <branch_name>`|Crear un nuevo `branch` o rama.|
|`git branch -l`|Listar todas las `branches`.|
|`git branch -D <branch_name>`|Eliminar una `branch`.|
|`git checkout <branch_name>`|Cambiar de `branch`.|
|`git diff <branch_A> <branch_B>`|Obtener las diferencias entre dos `branches`.|
|`git merge <branch_name>`|Mezclar `branch` indicada dentro de la `branch` actual. Métodos para mezclar: `fast forward`, `recursive`|

#### Notas:

- Se requiere un merge `fast forwar` cuando los cambios de diferentes ramas no estan en los mismos archivos.
- Se requiere un merge `recursive` cuando los cambios de diferentes ramas estan en los mismos archivos.

### Tag
|Command|Description|
|-------|-----------|
|`git tag`|Listar `tags`.|
|`git tag <tag_name>`|Crear un nuevo `tag`.|
|`git tag -a <tag_name> -m "<message\|annotation>"`|Crear un nuevo `tag` con anotación.|
|`git tag -a <tag_name> <hash> -m "<message\|annotation>"`|Crear un nuevo `tag` con anotación para un `commit` específico.|
|`git tag -d <tag_name>`|Eliminar `tag`.|
|`git show <tag_name>`|Mostrar los detalles de un `tag`.|

### Stash
|Command|Description|
|-------|-----------|
|`git stash`|Enviar todos los cambios actuales al `stash`.|
|`git stash save`|Enviar todos los cambios actuales al `stash`.|
|`git stash list`|Listar los `stashes`.|
|`git stash apply`|Recupera los cambios guardados en el ultimo `stash`.|
|`git stash apply <stash@{#}>`|Recupera los cambios guardados en un `stash` específico.|
|`git stash pop`|Recupera los cambios guardados en el ultimo `stash` y lo elimina de la lista de `stashes`.|
|`git stash drop`|Elimina el ultimo `stash`.|
|`git stash drop <stash@{#}>`|Elimina un `stash` específico.|

#### Options:

- `git stash save --keep-index` guarda todo menos los arhicovs en el `stage`.
- `git stash save --include-untracked` incluye todos los archivos, junto a los que git no le da seguimiento.
- `git stash save "<message>"` incluye un mensaje al `stash`.
- `git stash list --stat` muestra la lista de `stashes` con mas detalles.
- `git stash clear` elimina todos los stashes.

### Rebase
|Command|Description|
|-------|-----------|
|`git rebase <branch_name>`|Toma los `commits` diferentes de la rama actual los mueve a un area temporal, mientras mueve el `head` a la rama indicada para posteriormete poner encima los commits de la rama actual.|
|`git rebase -i <HEAD~#>\|hash`|Tomar el `commit` o `commits` indicados para interactuar con ellos.|

#### Uso del rebase interactivo:

- Ordernar commits
- Corregir mensajes de los commits
- Unir commits
- Separar commits

#### Comandos del rebase interactivo:
|Command|Description|
|-------|-----------|
|`p, pick`|Usar el `commit`.|
|`r, rework`|Usar el `commit` y editar el mensaje.|
|`e, edit`|Usar el `commit` y editar el contenido.|
|`s, squash`|Usar el `commit` y unirlo dentro del `commit` anterior.|
|`f, fixup`|Usar el `commit` y hacer `squash` pero sin solicitar mensaje.|
|`x, exec`|Ejecutar comando.|
|`d, drop`|Eliminar `commit`.|


### File
|Command|Description|
|-------|-----------|
|`git mv <file_name> <new_file_name>`|Renombrar o mover un archivo.|
|`git rm <file_name>`|Eliminar archivo.|

### Show
|Command|Description|
|-------|-----------|
|`git show <tag_name>`|Mostrar los detalles de un `tag`.|
|`git show <stash>`|Mostrar los detalles de un `stash`.|

### Help and others

|Command|Description|
|-------|-----------|
|`git version`|Obtener la versión de git.|
|`git help`|Obtener ayuda de los comandos de git.|
|`git help commit`|Obtener ayuda acerca del comando `commit`.|
|`git config --global alias.<alias> "<command>"`|Configurar un comando con un alias|
|`git config --global -l`|Listar configuraciones globales|
|`git config --global -e`|Editar configuraciones globales|
