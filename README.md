# Terminal and Command Line Course

## Terminal
- **Terminal**: window that shows us the promp, this hosts the shell.
- **Command line**: program that takes commands and passes them to the operating system to do something.

## Learning the terminal
| Command | Description |
| --------- | --------- |
| ls | List the files and folders from the directory |
| ls -l | List the diles and folders with all the info of each |
| ls -lh | List the diles and folders with all the info of each for human reading |
| cd | Moves the terminal to the home directory of the user |
| cd {folder} | Moves terminal to directory |
| clear | Cleans terminal (ctrl + l) |
| pwd | Print Working Directory. |
| file {name_file} | Describe the file's type |

## Manipulating files and directories

| Command | Description |
| --------- | --------- |
| ls -la | List all elements of directory, including hidden ones |
| ls -lS | Lists elements from highest to lowest size |
| ls -lr | Lists elements inversely |
| tree | Show all directories in tree form |
| tree -L {#} | Show all directories to the specified level |
| mkdir {folder} | Creates a new directory |
| touch {file} | Creates a new file |
| cp {original} {copia} | Copy file |
| mv {file} {path} | Move file to path |
| mv {name} {new_name} | Renames file or directory |
| rm {file} | Delete file |
| rm -i {file} | Delete file interactively (pide confirmación) |
| rm -r {folder} | Delete folder recursively |

## File content

| Command | Description |
| --------- | --------- |
| head {file} | Show the first 10 lines of file |
| head {file} -n {#} | Show the first n lines of file |
| tail {file} | Show the last 10 lines of file |
| tail {file} -n {#} | Show the last n lines of file |
| less {file} | Shows the file's content |
| xdg-open | Open file |
| nautilus | Open file system |


## What is a command

| Command | Description |
| --------- | --------- |
| type {command} | Show the command's category |
| alias {alias_name}="{command}" | Creates a termporal alias for a command |
| help {command} | Show info of how to use a command |
| man {command} | Show command's manual |
| info {command} | Show command's manual |
| whatis {command} | Show a short description of command |

## Wildcards

| Command | Description |
| --------- | --------- |
| ls *{.ext} | Filter files that end with extension |
| ls {word}* | Filter files that contain specific word |
| ls {word}? | Filter files that contain 1 character after word |
| ls [[:upper:]]* | Filter files and directories that start with uppercase on all the tree |
| ls -d [[:upper:]]* | Filter files and directories that start with uppercase on current directory |
| ls [[:lower:]]* | Filter files and directories that start with lowercase on all the tree |
| ls -d [[:lower:]]* | Filter files and directories that start with lowercase on current directory |
| ls [ad]* | Show files that start with `a` or `d` |

## Redirections

| Command | Description |
| --------- | --------- |
| ls {folder} > {name}.txt | Save list of files in directory in file.txt |
| ls {folder} >> {name}.txt | If files exist, concatenates list on file.txt |
| ls {folder} 2> {name}.txt | Redirect a stderr to file.txt |
| ls {folder} 2>&1 {name}.txt |Redirect stdout y stderr to file.txt |
| ls -lh \| less | Pipe operator allows a command's stdout to become the stdin of another command |
| echo "{text}" | Print text on terminal |
| cat {file} | Show a file's content |
| ls -ls \| sort | Order command's output |
| cowsay {text} | Print a cow saying the text |
| {command} \| lolcat | Colors output of command |


## Concatenating commands

| Command | Description |
| --------- | --------- |
| ls; mkdir NewFolder; cal | ; chains command to run synchronously |
| ls & date & cal | Commans are executed asynchronously |
| mkdir test && cd test | AND, if a command executes correctly then run the other command |
| cd test || touch file.txt | OR, executes only first command that runs correctly |

## Modify permissions on terminal
| Command | Description |
| --------- | --------- |
| chmod 755 {file_name} | Modifies permissions using octal mode |
| chmod u-r {file_name} | Removes permissions using symbolic mode |
| chmod u+r {file_name} | Gives permissions using symbolic mode |
| whoami | Returns the name of actual user |
| id | Groups the user belong to |
| su root | Changes to root user |
| sudo {command} | Gives root permissions to run command |
| passwd | Change password of current user |

## Environment variables

| Command | Description |
| --------- | --------- |
| printenv | List environment variables |
| echo $variable | Print the content of variable |

## Search commands

| Command | Description |
| --------- | --------- |
| which {bin} | Show path of binary |
| find {path} -name {name} | Search file on path |
| find {path} -type d -name {name} | Search directory on path that matches type and name |
| find {path} -type f -name {name} | Search file on path that matches type and name |
| find {path} -size 20M | Search on path a file with size |
| grep {expReg} {file} | Search all coincidences inside file (case sensitive) |
| grep -i {expReg} {file} | Search all coincidences inside file (not case sensitive)  |
| grep -c {expReg} {file} | Count number of occurrences |
| grep -v {expReg} {file} | Sind all non coincidences |
| wc {file} | Count number of lines, words and bits of file |
| wc -l {file} | Count only number of lines |
| wc -w {file} | Count only number of words |
| wc -c {file} | Count only number of bits |

## Network utilities

| Command | Description |
| --------- | --------- |
| ifconfig | Info of our network |
| ping {website} | Allows detection is a site is active or not |
| curl {website} | Return site's HTML |
| wget {website} | Downloads site's HTML on our computer |
| traceroute {website} | Trace route of all conexions to reach site |
| netstat -i | Show all network devices |

## Compressing files

| Command | Description |
| --------- | --------- |
| tar -cvf {name}.tar {folder} | Compress directory or file with .tar format |
| tar -cvzf {name}.tar.gz {folder} | Compress element with gzip |
| tar -xvf {name} | Decompress .tar |
| tar -xzvf {name} | Decompress gzip |
| zip -r {name}.zip {folder} | Compress element on .zip |
| unzip {name} | Decompress .zip |

## Process management

| Command | Description |
| --------- | --------- |
| ps | Show all processes running on terminal |
| kill {PID} | Stops process excecution |
| top | Show the processes using resources |

<!-- ## ¿Qué es la terminal?
- **Terminal**: es la ventanita que nos muestra el prompt. Este aloja la shell.
- **Línea de comandos**: programa que toma comandos y los pasa al sistema operativo para hacer algo.

## Aprendiendo a caminar en la terminal
| Comando | Descripción |
| --------- | --------- |
| ls | Lista los archivos y carpetas del directorio |
| ls -l | Lista los archivos y carpetas con toda la información de cada uno |
| ls -lh | Lista los archivos y carpetas con información para lectura humana |
| cd | Mueve la terminal al directorio home del usuario |
| cd {folder} | Mueve la terminal al directorio |
| clear | Limpia la pantalla de la terminal (ctrl + l) |
| pwd | Print Working Directory. Imprime la ruta del directorio actual |
| file {name_file} | Describe el tipo de archivo |

## Manipulando archivos y directorios

| Comando | Descripción |
| --------- | --------- |
| ls -la | Lista todos los elementos del directorio, incluyendo los ocultos |
| ls -lS | Listo los elementos ordenados por mayor a menor peso |
| ls -lr | Lista los elementos de manera inversa |
| tree | Despliega todos los directorios en forma de árbol |
| tree -L {#} | Despliega los elementos hasta el nivel ingresado |
| mkdir {folder} | Crea un nuevo directorio |
| touch {file} | crea un nuevo archivo |
| cp {original} {copia} | Copia un archivo |
| mv {file} {path} | Mueve el archivo a la ubicación ingresada |
| mv {name} {new_name} | Renombra el archivo o directorio |
| rm {file} | Elimina el archivo |
| rm -i {file} | Elimina de manera interactiva (pide confirmación) |
| rm -r {folder} | Elimina el directorio de manera recursiva |

## Explorando el contenido de nuestros archivos

| Comando | Descripción |
| --------- | --------- |
| head {file} | Muestra las primeras 10 líneas de un archivo |
| head {file} -n {#} | Muestra las primeras n líneas de un archivo |
| tail {file} | Muestra las últimas 10 líneas de un archivo |
| tail {file} -n {#} | Muestra las últimas n lineas de un archivo |
| less {file} | Muestra el contenido del archivo |
| xdg-open | Abre un archivo |
| nautilus | Abrir el sistema de archivos |


## ¿Qué es un comando?

| Comando | Descripción |
| --------- | --------- |
| type {command} | Muestra la categoria a la pertenece un comando |
| alias {alias_name}="{command}" | Crea un alias temporal para un comando |
| help {command} | Muestra información de cómo usar el comando |
| man {command} | Muestra el manual del comando |
| info {command} | Muestra el manual del comando |
| whatis {command} | Muestra una descripción corta del comando |

## Wildcards

| Comando | Descripción |
| --------- | --------- |
| ls *{.ext} | Filtra archivos que terminen con la extensión |
| ls {word}* | Filtra archivos que contengan una palabra especifica |
| ls {word}? | Filtra archivos que contengan 1 caracter despues de la palabra |
| ls [[:upper:]]* | Filtra archivos y directorios que inicen con mayuscula en todo el arbol |
| ls -d [[:upper:]]* | Filtra archivos y directorios que inicen con mayuscula en el directorio actual |
| ls [[:lower:]]* | Filtra archivos y directorios que inicen con minuscula en todo el arbol |
| ls -d [[:lower:]]* | Filtra archivos y directorios que inicen con minuscula en el directorio actual |
| ls [ad]* | Muestra los archivos que comiencen con a o d |

## Redirecciones

| Comando | Descripción |
| --------- | --------- |
| ls {folder} > {name}.txt | La lista de archivos del directorio se guarda en el archivo .txt |
| ls {folder} >> {name}.txt | Si el archivo ya existe, el listado se concatena al contenido del archivo .txt |
| ls {folder} 2> {name}.txt | Redirige un stderr a una salida por archivo |
| ls {folder} 2>&1 {name}.txt | Redirige el stdout y stderr a una salida por archivo |
| ls -lh \| less | El pipe operator permite que el stdout de un comando se contierta en el stdin de otro |
| echo "{text}" | Imprime en consola el text |
| cat {file} | Muestra el contenido de un archivo |
| ls -ls \| sort | Ordena la salida del comando |
| cowsay {text} | Imprime una vaca diciendo el texto |
| {command} \| lolcat | Colorea la saida del comando |


## Encatenando comandos

| Comando | Descripción |
| --------- | --------- |
| ls; mkdir NewFolder; cal | ; encadena comandos para que se ejecuten de forma síncrona |
| ls & date & cal | Se ejecutan de manera asíncrona |
| mkdir test && cd test | AND, si se cumple cun comando entonces se ejecuta el siguiente |
| cd test || touch file.txt | OR, se ejecuta solo el primer comando que cumpla |

## Modificando permisos en la terminal

| Comando | Descripción |
| --------- | --------- |
| chmod 755 {file_name} | Modifica permisos con el modo octal |
| chmod u-r {file_name} | Quita permisos con el modo simbólico |
| chmod u+r {file_name} | Modifica permisos con el modo simbólico |
| whoami | Devuelve el nombre del usuario actual |
| id | Grupos a los que pertenece el usuario |
| su root | Cambia al usuario root |
| sudo {command} | Da permisos de root para ejecutar el comando |
| passwd | Cambia la contraseña del usuario actual |

## Variables de entorno

| Comando | Descripción |
| --------- | --------- |
| printenv | Lista las variables de entorno |
| echo $variable | Imprime el contenido de la variable |

## Comandos de búsqueda

| Comando | Descripción |
| --------- | --------- |
| which {bin} | Muestra la ruta del binario |
| find {path} -name {name} | Busca en la ruta el archivo |
| find {path} -type d -name {name} | Busca en la ruta un directorio que coincida con el tipo y nombre |
| find {path} -type f -name {name} | Busca en la ruta un archivo que coincida con el tipo y nombre |
| find {path} -size 20M | Busca en la ruta un archivo con el peso |
| grep {expReg} {file} | Busca todas las coincidencias dentro del archivo (case sensitive) |
| grep -i {expReg} {file} | Busca todas las coincidencias dentro del archivo (no case sensitive)  |
| grep -c {expReg} {file} | Cuenta el número de ocurrencias |
| grep -v {expReg} {file} | Encontrar todas las no coincidencias |
| wc {file} | Cuenta la cantidad de líneas, palabras y bits de un archivo |
| wc -l {file} | Cuenta solo el número de líneas |
| wc -w {file} | Cuenta solo el número de palabras |
| wc -c {file} | Cuenta solo el número de bits |

## Utilidades de red

| Comando | Descripción |
| --------- | --------- |
| ifconfig | Información de nuestra red |
| ping {website} | Permite detectar si una página está activa o no |
| curl {website} | Devuelve el HTML del sitio |
| wget {website} | Descarga el HTML directamente a nuestra computadora |
| traceroute {website} | Traza la ruta de todas las conexiones realizadas para llegar al sitio |
| netstat -i | Nos muestra los dispositivos de red |

## Comprimiendo archivos

| Comando | Descripción |
| --------- | --------- |
| tar -cvf {name}.tar {folder} | Comprime el directorio o archivo al formato .tar |
| tar -cvzf {name}.tar.gz {folder} | Comprime el elemento con formato gzip |
| tar -xvf {name} | Descomprime .tar |
| tar -xzvf {name} | Descomprime gzip |
| zip -r {name}.zip {folder} | Comprime el elemento con formato .zip |
| unzip {name} | Descomprime .zip |

## Manejo de procesos

| Comando | Descripción |
| --------- | --------- |
| ps | Muestra los procesos corriendo en la terminal |
| kill {PID} | Detiene la ejecución de un proceso |
| top | Muestra los procesos que están usando más recursos | -->
