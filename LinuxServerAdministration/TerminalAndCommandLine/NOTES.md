# Notas - Terminal y Línea de Comandos
Notas auxiliares sobre la Terminal y la Línea de Comandos, como comandos más utilizados, permisos de usuarios, etc.
## Comandos más comunes
* Listar contenido del directorio (archivos y subdirectorios) ordenados alfabeticamente
```
ls
```
* Listar contenido del directorio incluyendo los que se han definido como ocultos
```
ls -a
```
* Listar contenido del directorio con detalles: usuario, grupo, permisos, tamaño, fecha y hora de creación
```
ls -l
```
* Listar contenido del directorio con detalles pero con las unidades de tamaño en KB, MB
```
ls -lh
```
* Listar contenido del directorio con detalles y ordenado por tamaño de manera descendente
```
ls -lS
```
* Listar contenido del directorio con detalles y ordenado por fecha de modificación de manera descendente
```
ls -lt
```
* Listar contenido del directorio con detalles y ordenado alfabeticamente primero por nombre y después por extensión
```
ls -lx
```
* Listar contenido del directorio con detalles con orden inverso
```
ls -lr
```
```
ls -lSr
```
```
ls -ltr
```
```
ls -lXr
```
* Listar contenido de todos los subdirectorios de forma recursiva
```
ls -R
```
* Mostrar directorio actual
```
pwd
```
* Cambiar de directorio
```
cd /ubicación/del/directorio
```
* Cambiar de directorio al directorio home
```
cd ~ 
```
* Cambiar de directorio al último directorio visitado
```
cd -  
```
* Crear directorio
```
mkdir nombre_del_directorio
```
* Copiar archivo a directorio
```
cp /ubicación/del/archivo/nombre_del_archivo /ubicación/del/directorio
```
* Eliminar archivo dentro de un directorio
```
rm /ubicación/del/archivo/nombre_del_archivo
```
* Mover archivo a directorio
```
mv /ubicación/del/archivo/nombre_del_archivo /ubicación/del/directorio
```
* Eliminar directorio vacío
```
rmdir /ubicación/del/directorio/vacío
```
* Eliminar directorio y todo su contenido recursivamente sin solicitar confirmación por cada archivo borrado
```
rm -rf /ubicación/del/directorio
```
* Crear archivo
```
touch /ubicación/del/archivo/nombre_del_archivo
```
* Mostrar el contenido de un archivo de texto
```
cat /ubicación/del/archivo/nombre_del_archivo
```
* Mostrar las primeras 10 lineas de un archivo de texto
```
head /ubicación/del/archivo/nombre_del_archivo
```
* Mostrar las primeras n lineas de un archivo de texto
```
head -n [numero de lineas] /ubicación/del/archivo/nombre_del_archivo
```
* Mostrar las ultimas 10 lineas de un archivo de texto
```
tail /ubicación/del/archivo/nombre_del_archivo
```
* Mostrar las ultimas n lineas de un archivo de texto
```
tail -n [numero de lineas] /ubicación/del/archivo/nombre_del_archivo
```
* Filtrar contenido de texto línea por línea contra con una expresión regular
```
grep [regex] /ubicación/del/archivo/nombre_del_archivo
```
* Filtrar contenido de texto línea por línea contra con una expresión regular ignorando mayúsculas o minúsculas
```
grep -i [regex] /ubicación/del/archivo/nombre_del_archivo
```
## Comandos para Manejo de Archivos de Texto
### Vim
* Editar un archivo de texto o crear uno nuevo con Vim
```
vim /ubicación/del/archivo/nombre_del_archivo
```
* Editar texto, entrar al modo de edición
```
i
```
* Salir del modo de edición
```
Presionar Esc
```
* Activar uso de comandos
```
:
```
* Guardar los cambios en el archivo
```
:w
```
* Salir de vim
```
:q
```
* Guardar los cambios en el archivo y salir de vim
```
:x
```
### Nano
* Editar un archivo de texto o crear uno nuevo con Nano
```
nano /ubicación/del/archivo/nombre_del_archivo
```
* Guardar los cambios en el archivo
<kbd>Ctrl</kbd> + <kbd>O</kbd>
* Salir de nano
<kbd>Ctrl</kbd> + <kbd>X</kbd>
## Shortcuts
* Buscar en el historial de comandos: <kbd>Ctrl</kbd> + <kbd>R</kbd>
* Limpiar la terminal: <kbd>Ctrl</kbd> + <kbd>L</kbd>
* Salir de la terminal: <kbd>Ctrl</kbd> + <kbd>D</kbd>
* Detener el comando o proceso: <kbd>Ctrl</kbd> + <kbd>C</kbd>
