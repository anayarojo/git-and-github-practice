# Practice with Git and Github

|Command|Description|
|-------|-----------|
|`git version`|Obtener la versión de git.|
|`git help`|Obtener ayuda de los comandos de git.|
|`git help commit`|Obtener ayuda acerca del comando `commit`.|
|`git config --global user.name <name>`|Configurar globalmente el nombre de usuario.|
|`git config --global user.email <email>`|Configurar globalmente el correo electrónico.|
|`git init`|Iniciar git en un nuevo proyecto.|
|`git status`|Obtener el estado de los archivos en git.|
|`git status -s`|Obtener el estado de los archivos en git, omitiendo datos innecesarios.|
|`git status -s -b`|Obtener el estado de los archivos en git, omitiendo datos innecesarios, incluyendo los nombres de las ramas.|
|`git add <.\|--all\|-A>`|Agregar todos los archivos al stage.|
|`git add <*.extension\|folder/*.extension>`|Agregar todos los archivos, de una extension específica, al stage.|
|`git add <folder/>`|Agregar todos los archivos, de una carpeta específica, al stage.|
|`git add <file>`|Agregar archivo específico al stage.|
|`git reset <.\|--all\|-A>`|Quitar todos los archivos del stage.|
|`git reset <*.extension\|folder/*.extension>`|Quitar todos los archivos, de una extension específica, del stage.|
|`git reset <folder/>`|Quitar todos los archivos, de una carpeta específica, del stage.|
|`git reset <file>`|Quitar archivo específico del stage.|
|`git commit -m <message>`|Agregar un nuevo `commit`|
|`git checkout -- <.>`|Establecer el proyecto con el ultimo `commit`|
|`git config --global alias.<alias> "<command>"`|Configurar un comando con un alias|
|`git config --global -l`|Listar configuraciones globales|
|`git config --global -e`|Editar configuraciones globales|
|`git diff`|Lista las diferencias respecto al ultimo `commit`.|
|`git diff --stage`|Lista las diferencias del `stage` respecto al ultimo `commit`.|
|`git reset HEAD <File>`|Quitar archivo del `stage`.|
|`git checkout -- <File>`|Recuperar un archivo desde el ultimo `commit`.|
|`git commit --amend -m "<New message>"`|Cambiar el mensaje del ultimo `commit`.|
|`git reset --soft HEAD^`|Deshacer el ultimo commit sin eliminar los cambios.|

