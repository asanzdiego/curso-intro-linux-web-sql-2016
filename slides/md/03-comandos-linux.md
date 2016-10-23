% Comandos Linux
% Adolfo Sanz De Diego
% Noviembre 2016




# Acerca de




## Autor

- **Adolfo Sanz De Diego**
    - Blog: [asanzdiego.blogspot.com.es](http://asanzdiego.blogspot.com.es/)
    - Correo: [asanzdiego@gmail.com](mailto:asanzdiego@gmail.com)
    - GitHub: [github.com/asanzdiego](http://github.com/asanzdiego)
    - Twitter: [twitter.com/asanzdiego](http://twitter.com/asanzdiego)
    - LinkedIn: [in/asanzdiego](http://www.linkedin.com/in/asanzdiego)
    - SlideShare: [slideshare.net/asanzdiego](http://www.slideshare.net/asanzdiego/)

## Licencia

- **Este obra está bajo una licencia:**
    - [Creative Commons Reconocimiento-CompartirIgual 3.0](http://creativecommons.org/licenses/by-sa/3.0/es/)

## Fuente

- Las slides y sus fuentes las podéis encontrar en:
    - <https://github.com/asanzdiego/curso-intro-linux-web-sql-2016>




# Comandos básicos




## Cambio de directorio

- Para cambiar de directorio se usa el comando **cd
directorio_destino**.

- Usamos **cd ..** para ir al directorio
superior.

- Usamos **cd sin argumentos** para
volver a la carpeta personal.

##  Situación actual

- El comando **pwd** imprime la ruta del directorio en el
que nos encontramos en este momento.

## Listado

- El comando **ls** muestra los nombres de los ficheros y
subdirectorios contenidos en el directorio en el que
se está. Sólo se obtienen los nombres de los
ficheros, sin ninguna otra información.

## Listas ocultos

- El comando **ls -a** muestra todos los ficheros incluyendo
algunos que están ocultos para el usuario
(aquellos que comienzan por un punto).

- Observar que el fichero punto . indica el directorio actual y
el doble punto .. el directorio padre, que contiene
al actual.

## Listado ordenados

- **ls -c** muestra ordenando por día y hora de creación.
- **ls -t** muestra ordenando por día y hora de modificación.
- **ls -r** muestra el directorio y lo ordena en orden inverso.
- **ls subdir** muestra el contenido del subdirectorio subdir.

## Otros listados

- **ls --color** muestra el contenido del directorio coloreado: verde para los ejecutables,azul las
carpetas, fucsia las imagenes, rojo los comprimidos, ...
- **ls -l** muestra toda la información de cada fichero incluyendo: protecciones, tamaño y fecha de
creación o del último cambio introducido,...

## Combinación de opciones

- Las opciones anteriores pueden combinarse como
por ejemplo **ls -cr** que muestra el directorio
ordenando inversamente por fechas.

## Filtrado

- Muchos comandos admite los caracteres de sustitución:
    - **\* que representa cualquier conjunto o secuencia de
caracteres**
    - y **? que representa cualquier carácter pero sólo uno**.

- Por ejemplo **ls \*.gif** muestra todos los nombres de
ficheros que acaben en .gif y **ls file?** muestra todos
los ficheros cuyos nombres empiecen por file y
tengan un nombre de cinco caracteres.

## Creación de subdirectorios

- El comando **mkdir** permite crear un nuevo
subdirectorio. La sintaxis es mkdir subdir1 donde
subdir es el nombre del directorio que se va a crear.

## Borrado de subdirectorios

- El comando **rmdir** borra uno o más directorios del
sistema siempre que estos subdirectorios estén
vacíos. La sintaxis es rmdir subdir1 donde subdir es
el nombre del directorio que se va a eliminar.

## Copia de ficheros

- El comando **cp** permite hacer la copia de un fichero.
La sintaxis del comando es cp file1 file2 que indica
que hace una copia de file1 y le llama file2. Si file2
no existía, lo crea con los mismos atributos de file1, y
en caso de existir su contenido es sustituido por el
de file1. El fichero file2 estará en el mismo directorio
que file1.

## Mover/renombrar fichero

- El comando **mv** permite mover o renoimbrar un fichero.
La sintaxis es mv file1 file2 y realiza la misma función que
cp pero eliminando el fichero original. Desde la visión del
usuario, se cambia el nombre a file1 por file2.

- Si los nombres que aparecen son de directorios entonces
el comando mv namedir1 namedir2 cambia el nombre
del subdirectorio namedir1 por namedir2.

## Enlaces

- Un mismo fichero puede estar repetido con más de
un nombre y poder acceder a él desde más de un
directorio. Esto último se denomina enlaces
múltiples a un fichero, y se crean con el comando **ln**:
ln file1 file2
Así el fichero file1 tiene dos nombres: file1 y file2.

## Borrado de ficheros

- El comando **rm** elimina uno o más ficheros de un
directorio en el cual tengamos permiso de escritura.
La sintaxis es rm file1 file2

## Permisos

- Los permisos de cada fichero se pueden ver con el
comando ls -l.

- Estos permisos son:
    - **r**: de lectura (o listar en directorios)
    - **w**: de escritura (o crear y borrar ficheros en directorios)
    - **x**: de ejecución (o buscar y utilizar ficheros en directorios)

## Cambiar permisos

- Para cambiar los permisos de un
fichero se emplea el comando **chmod [quien] operacion permiso file** donde:
    - quien: indica a quien afecta el permiso que se
    desea cambiar:
        - **u**: para el usuario propietario del archivo,
        - **g**: para el grupo del usuario propietario del archivo,
        - **o**: para los otros usuarios
        - **a**: para todos los anteriores. (valor por defecto).
    - oper: indica si el permiso se da usando un + o se
    quita usando un -.

## Cambiar dueño

- El comando **chown** se emplea para cambiar de
propietario a un determinado conjunto de ficheros:
chown newowner file1 file2 ...
- Sólo lo puede emplear el actual propietario de los
mismos.
- Los nombres de propietario se encuentran
almacenados en el fichero **/etc/passwd**.

## Cambio de grupo

- El comando **chgrp** se emplea para cambiar el grupo
al que pertenece un fichero : chgrp newgroup file1
file2...
- Los grupos de usuarios están almacenados en el
fichero **/etc/group**.

## Visualización con cat

- El comando **cat filename** permite visualizar el
contenido de uno o más ficheros de forma no
formateada, y copiar uno o más ficheros como
apéndice de otro ya existente.

## Concatenar ficheros

- **cat file1 file2 >file3**: El contenido de los ficheros file1 y file2
es almacenado en file3.
- **cat file1 file2 >>file3**: el contenido de file1 y file2 es añadido
al final de file3.
- **cat >file1**: Acepta lo que se introduce por el teclado y lo
almacena en file1 (se crea file1). Para terminar se emplea
<ctrl>d

## Visualización con more

- El comando **more filename** permite visualizar el
contenido de un fichero pantalla pantalla.

- Para pasar de pantalla se utiliza la barra espaciadora o la tecla enter.

- Para salir se pulsa <ctrl>d o q.

## Visualización con less

- El comando **lessº filename** permite visualizar el
contenido de un fichero pantalla pantalla.

- Para pasar de pantalla se utilizan las flechas arriba y abajo.

- Para salir se pulsa <ctrl>d o q.

## Búsqueda en ficheros

- El comando **grep 'conjuntocaracteres' file1 file2 file3**
busca una palabra, clave o frase en un conjunto de
directorios, indicando en cuáles de ellos la ha
encontrado.

- Se pueden utilizar expresiones regulares de la forma:
grep [-opcion] expresión_regular [referencia...]

## Opciones grep

- **c**: escribe el número de las líneas que satisface la
condición.
- **i**: no se distinguen mayúsculas y minúsculas.
- **l**: escribe los nombres de los ficheros que contienen
líneas buscadas.
- **n**: cada línea es precedida por su número en el

## Mas opciones grep

- **s**: no se vuelcan los mensajes que indican que un
fichero no se puede abrir.
- **v**: se muestran sólo las líneas que no satisfacen el
criterio de selección.

## Ejemplos grep

- **grep ‘ˆd’ text** recupera las líneas que comienzan por d.
- **grep ‘ˆ[ˆd]’ text** recupera las líneas que no comienzan por d.
- **grep -v ‘ˆC’ file1 > file2** quita las líneas de file1 que comienzan por C y lo copia en file2.

## Comandos básicos del terminal

- Redirecciones:
Se puede redirigir la salida de un comando usando
los operadores:
•(>) redirige la salida estándar hacia el fichero
indicado y en caso de no existir se crea.
•(<) redirige la entrada estándar desde un
determinado fichero
•(>>) redirige la salida estándar hacia otro fichero,
pero añadiendo dicha salida al final de ese fichero,
sin sobreescribir el contenido original.

## Comandos básicos del terminal

- Redirecciones:
Por ejemplo:
•date >>archivo el fichero archivo contendrá
información sobre todas las veces que hemos
entrado en el sistema.
•cat file1 file2 >file3 añade al fichero file2 al final de
file1 y al conjunto lo llama file3
•cat file2 >>file1 realiza la misma operación que el
anterior, pero al resultado lo llama file1

## Comandos básicos del terminal

- Tuberías
Una tubería (|)
permite comunicar la salida
estándar de un comando con la entrada estándar de
otro.
Por ejemplo
ls | mail juan envía a
juan una lista de los ficheros del sistema.
Con el operador de tubería se pueden empalmar
tantos comandos como se desee.

## Comandos básicos del terminal

- Ejecución de un programa
Existen varios comandos para gestionar la ejecución
de un programa:
- El carácter & permite realizar una ejecución en
segundo plano recuperando inmediatamente el
control del terminal. Para ello se añade el carácter
& al final del comando de ejecución program <
datos.d >resultados.r &. Como resultado aparece
en el terminal el número de proceso de la
ejecución de este programa.

## Comandos básicos del terminal

- Ejecución de un programa
- Para detener la ejecución de un proceso se puede
utilizar el comando kill númerodeproceso
- Cuando se sale del sistema si hay algún proceso
ejecutándose en segundo plano se para salvo que
se use el comando nohup program. En este caso
todas las salidas del programa se dirigen a un
fichero llamado nohup.out.

## Comandos básicos del terminal

- Ejecución de un programa
- El comando nice permite realizar ejecuciones con
baja prioridad de la forma:
- **nice program &
- **nice nohup program &
Para darle al programa la prioridad mínima habría
que invocarlo como nice -19 program & donde el
-19 indica la mínima prioridad.

## Comandos básicos del terminal

- Ejecución de un programa
- El comando top muestra una lista de los procesos
que se están ejecutando.

## Comandos básicos del terminal

- Compresión de ficheros
El comando tar –cvf nombre_archivo.tar
fichero1 fichero2 … agrupa varios ficheros en
uno solo “archivo” tar, y gzip fichero se
comprime fichero (que es borrado) y se crea un
fichero con nombre fichero.gz.

## Comandos básicos del terminal

- Compresión de ficheros
Dado que suele emplearse tar y gzip de forma
consecutiva obteniéndose archivos con extensión
tar.gz o tgz, entonces tar incluye la opción z para
extraer ficheros con esta extensión
tar –
zxf fichero.tar.gz

## Comandos básicos del terminal

- Compresión de ficheros
Se pueden realizar las operaciones inversas, de
manera que se pueden extraer los ficheros
mediante
tar –xpvf
nombre_archivo.tar fichero1 …, y descomprimir
un fichero mediante gzip –d fichero.gz

## Otros comandos
- Espacio ocupado en el disco.
El comando du permite conocer el espacio en
bloques ocupado en el disco por un determinado
directorio y todos los subdirectorios que cuelgan de
él. Para usarlo se coloca en el directorio y se teclear
du:

## Otros comandos
- Espacio ocupado en el disco.
Para obtener la información en bytes se debe
emplear la opción –h: du -h

## Otros comandos
- Espacio ocupado en el disco.
El comando df informa del espacio usado por las
particiones del sistema que se encuentren
montadas.

## Otros comandos
- Otros comandos
Comando

Significado

date

Muestra el día y la hora

cal

Muestra el calendario. Tiene diversas opciones.
Por ejemplo cal 1945 mostraría el calendario del
año 1945.

who

Indica qué usuarios tiene el ordenador en ese
momento, en qué terminal están y desde qué
hora.

whoami

Indica cuál es la terminal y la sesión en la que se
está trabajando.

## Otros comandos
- Otros comandos
Comando

Significado

uptime

Muestra el tiempo que lleva encendido nuestro
ordenador.

hostname

Muestra el nombre de la maquina

bc

Abre una calculadora de texto. Para salir se
introduce quit.

lshw

Muestra todas las características del hardware.

## Otros comandos
- Otros comandos
Comando

Significado

history

Muestra los comandos usados por el usuario
en orden cronológico

fc -l

Muestra los últimos comandos usados por el
usuario

man comando

Muestra el manual de un comando con sus
modificadores y argumentos.

lspci

Muestra los diferentes dispositivos PCI.

## Otros comandos
- Otros comandos
Comando

Significado

umask

Muestra los permisos con los que el usuario
creara sus archivos por
defecto

uname -r

Muestra la version del kernel

lsusb

Muestra los dispositivos tengo en los bus
USB

xkill

Permite cerrar un programa bloqueado.

## Otros comandos
- Otros comandos
Comando

Significado

groups

Muestra los grupos del sistema alos que
pertenece un usuario.

clear

Limpia la consola.

head

Indicando un número n y un nombre de fichero,
muestra las n primeras líneas del fichero
indicado.

##
