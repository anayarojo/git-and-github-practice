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

### File
|Command|Description|
|-------|-----------|
|`git mv <file_name> <new_file_name>`|Renombrar o mover un archivo.|
|`git rm <file_name>`|Eliminar archivo.|

### Help and others

|Command|Description|
|-------|-----------|
|`git version`|Obtener la versión de git.|
|`git help`|Obtener ayuda de los comandos de git.|
|`git help commit`|Obtener ayuda acerca del comando `commit`.|
|`git config --global alias.<alias> "<command>"`|Configurar un comando con un alias|
|`git config --global -l`|Listar configuraciones globales|
|`git config --global -e`|Editar configuraciones globales|
