# Curso Terminal y Linea de Comandos

## ¿Qué es la terminal?
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
| top | Muestra los procesos que están usando más recursos |
