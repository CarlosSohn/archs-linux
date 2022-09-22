# Arch-Linux
Este proyecto contiene un arbol de directorios que sirven para practicar comandos de gestión de ficheros en Linux.

# Practica 1
Crea, modifica, copia, mueve, renombra y elimina archivos en la linea de comados.
## Ejercicio 1 
	1. Cada uno de los siguientes puntos se debe hacer usando rutas absolutas. Sólo se pueden usar los comandos ls y mkdir
	2. Ordena los archivos del directorio 'analisis'. Se debe crear un directorio por cada conjunto de nombres. Por ejemplo, los archivos r-1.1 y r-1.2 deben estar en un nuevo directorio con el nombre de r-1
	3. Ordena los archivos del directorio 'documentation'. Se debe crear un nuevo directorio por cada conjunto de nombres. Lo mismo que el ejemplo del punto anterior.
	4. Ordena los archivos del directorio 'exec'. Se debe crear un nuevo directorio por cada conjunto de nombres. Lo mismo que el ejemplo del punto anterior.
	5. Ordena los archivos del directorio 'source'. Se debe crear un nuevo directorio por cada conjunto de nombres. Lo mismo que el ejemplo del punto anterior.
	6. Ordena los archivos del directorio 'pruebas' por fecha de creación. Se debe crear un directorio por cada año y un subdirectorio por mes. Por ejemplo, si un archivo se creo en Mayo de 2006, entonces se crea un directorio '2006' y un subdirectorio 'Mayo'

## Ejercicio 2
	1. Cada uno de los siguientes puntos se debe hacer usando rutas absolutas. Sólo se pueden usar los comandos cp, mv, rm, touch y  vim o nano
	2. En el directorio 'Documentos' crea un subdirectorio 'backup'. Dentro de 'backup' crea los subdirectorios 'v1', 'v2', v3.
	3. Copia todo lo relacionado con v1 en el directorio v1. Esto incluye todos los archivos que tiene 'v1' en su nombre. Ejemplos de lo que puede haber en este directorio son 'v1.1' 'r-v1.2', 'v1-doc', etc.
	4. Copia todo lo relacionado con v2 en el directorio v2. Esto incluye todos los archivos que tiene 'v2' en su nombre. Mira los ejemplos del punto 3
	5. Copia todo lo relacionado con v3 en el directorio v3. Esto incluye todos los archivos que tiene 'v3' en su nombre. Mira los ejemplos del punto 3
	6. Mueve todos los archivos del directorio 'pruebas' al directorio 'backup'
	7. Localiza y elimina los archivos 'recursividad.c', 'libssl.c' y 'udp.c' de la carpeta 'pruebas'. Después, elimina directorios vacios, si los hay.
	8. Crea un nuevo archivo en 'backup' llamado 'README.md'. El contenido del archivo debe ser los siguiente: 'En este directorio está el respaldo actualizado de mi proyecto'.
	9. Cambia el nombre de los directorios 'vn' (que estan en 'backup') por 'version-n', donde 'n' es un número entre 1 y 3. Por ejemplo, el directorio 'v1' debe ser 'version-1'

# Practica 2
Compresión de ficheros y carpetas
## Ejercicio 1
	1. Para este ejercicios se pueden usar rutas absolutas y/o relativas.
	2. Elige una herramienta de comprensión de archivos (gzip, bzip2 o xz) y comprime todos los archivos individuales en tanto en 'backup' como en sus subdirectorios, manteniendo los archivos originales. Por ejemplo, después de comprimir 'archivo' con xz, debes tener en el directorio tanto 'archivo' como 'archivo.xz'.
	3. Dentro de cada subdirectorio de 'backup' crea un subdirectorio 'comprimido', donde deverás mover todos los archivos comprimidos
	4. Comprime cada subdirectorio 'comprimido' que exista en 'backup'.
	5. Comprime cada subdirectorio dentro de 'backup'
	6. Comprime 'backup' y encriptalo
	7. Observa la diferencia en tamaño entre 'backup' y el archivo resultante del punto 6.

## Ejercicio 2
	1. Mueve el archivo resultante del punto 6 del ejercicio anterior a una carpeta diferente.
	2. Restaura todos los archivos comprimidos. El resultado de esta actividad debe ser igual al directorio original 'backup'. No debe haber más ni menos archivos.

# Practica 3
Trabajar con copias de seguridad
## Ejercicio 1
	1. Realiza los siguientes puntos empleado unicamente el comando cpio
	2. Crea una copia de seguridad del directorio 'backup'.
	3. Lista el contenido de la copia que realizaste en el punto anterior
	4. Crea un nuevo directorio 'cpio' y, dentro, restaura la copa de seguridad que creaste en el punto 2 
## Ejercicio 2
	1. Realiza los siguientes puntos empleado unicamente el comando tar
	2. Crea una copia COMPLETA de 'backup'.
	3. Lista el contenido de la copia que realizaste en el punto anterior
	4. Añade contenido a cada uno de los archivos en /pruebas
	5. Crea una copia DIFERENCIAL de 'backup'
	6. Deshaz los cambios del punto 4. Los archivos de 'pruebas' deben estar como antes (sin contenido).
	7. Elimina 'backup'
	8. Haz una restauración completa de 'backup' (COMPLETA+DEFIRENCIAL)

# Practica 4
Gestionar propietarios y permisos de archivos

## Ejercicio 1
	1. Para este ejericicio se deben usar el comando chown
	2. Cambia el usuario y grupo propietario del directorio 'backup', junto ocn todos sus archivos. El nuevo usuario/grupo debe ser root/root. 
	3. Cambia el usuario propietario de todos los archivos que hay en 'pruebas', dentro de backup. El nuevo propietario debes ser tu.
	4. Cambia el grupo propietario de todos los archivos que hay en 'exec', dentro de 'backup'. El nuevo grupo propieatario debe ser el tuyo.

# Ejercicio 2
	1. Para este ejericicio se deben usar el comando chmod. Puedes usar la manera octal o simbolica, a menos que se indique lo contrario.
	2. Establece los siguientes permisos para cada archivo de 'analisis', dentro de 'backup'. Debes usar la manera simbólica
		- usuario propietario sólo puede leer y escribir
		- grupo propietario sólo puede leer
		- El resto sólo puede leer
	3. Establece los siguientes permisos para cada archivo de 'documentation', dentro de 'backup'. Debes usar la manera octal
		- usuario propietario tiene todos los permisos
		- grupo propietario sólo puede ejecutar
		- El resto sólo puede escribir
	4. Establece los siguientes permisos para cada archivo de 'exec', dentro de 'backup'. Debes usar la manera octal
		- usuario propietario tiene todos los permisos
		- grupo propietario sólo puede ejecutar y leer
		- El resto sólo puede escribir y ejecutar
	5. Haz que nadie puede ejecutar ningún archivo de 'exec', excepto tu.
	6. Haz que sólo los miembros del grupo puedan puedan leer los archivos en 'documentation'. Los miembros del grupo no pueden escribir ni ejecutar.
	7. Haz que sólo tu puedas ver el contenido del directorio 'source'
