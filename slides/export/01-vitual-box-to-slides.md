% VirtualBox
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





# VirtualBox





## ¿Qué es?

- Programa de Software Libre.

- Permite **instalar un Sistema Operativo dentro de otro**.

## Descarga

- https://www.virtualbox.org/wiki/Downloads

![Descarga de VirtualBox](../img/01-virtual-box/01-virtual-box-01.png)

## Instalación

- Elegir la versión adecuada para el Sistema Operativo que tenemos instalado.

- Intalar de la forma habitual dependiendo del Sistema Operativo instalado.




# Descargar Ubuntu




## Ubuntu

- Ubuntu es una **districución Linux** muy utilizada.

## Enlace

- http://www.ubuntu.com/download/desktop

![Enlace de Ubuntu](../img/01-virtual-box/01-ubuntu-01.png)

## Donativo

- Al pulsar el botón "Download", nos lleva a una página para realizar una donación,
y si no queremos donar y continuar pulsamos
en la parte inferior en "**Not now, take me to the download**".

![Donativo de Ubuntu](../img/01-virtual-box/01-ubuntu-02.png)

## Descarga

- La descarga coomenzará automáticamente, pero si no lo hiciera
pulsamos sobre "**download now**".

![Descarga de Ubuntu](../img/01-virtual-box/01-ubuntu-03.png)




# Crear Máquina Virtual




## Abrir VirtualBox

- Abrimos **VirtualBox**:

![Abrir VirtualBox](../img/01-virtual-box/01-virtual-box-02.png)

## Nueva Máquina Virtual

- Pulsamos sobre "**Nueva**" para añadir una nueva máquina virtual.

![Nueva Máquina Virtual](../img/01-virtual-box/01-virtual-box-03.png)

## Nombre Máquina Virtual

- En el asistente insertamos en el nombre "**Ubuntu**".

![Nombre Máquina Virtual](../img/01-virtual-box/01-virtual-box-04.png)

## Memoria Máquina Virtual

- Elegimos la cantidad de **memoria** reservada a Ubuntu:

![Memoria Máquina Virtual](../img/01-virtual-box/01-virtual-box-05.png)

## Crear Disco Virtual

- Seleecionamos "**Crear disco virtual ahora**".

![Crear Disco Virtual](../img/01-virtual-box/01-virtual-box-06.png)

## Tipo Disco Virtual

- Seleccionamos **VDI(VirtualBox Disk Image)**.

![Tipo Disco Virtual](../img/01-virtual-box/01-virtual-box-07.png)

## Tipo Almacenamiento

- Seleccionamos "**Reservado dinámicamente**".

![Tipo Almacenamiento](../img/01-virtual-box/01-virtual-box-08.png)

## Ubicación y Tamaño

- Podemos seleccionar **la ubicación y el tamaño** del disco virtual.

![Ubicación y Tamaño](../img/01-virtual-box/01-virtual-box-09.png)

## Finalizar

- Si todo ha salido bien nos aparecerá la **máquina recién creada** en VirtualBox.

![Listar Máquina Virtual](../img/01-virtual-box/01-virtual-box-10.png)




## Configurar Máquina Virtual




## Abrir configuración

- Seleccionamos máquina recién creada y pulsamos en "**Configuración**".

![Abrir configuración](../img/01-virtual-box/01-virtual-box-11.png)

## Configurar almacenamiento

- Pulsamos sobre "**Almacenamiento**".

![Configurar almacenamiento](../img/01-virtual-box/01-virtual-box-12.png)

## Seleccionar CD Virtual

- Pulsamos sobre el **icono "CD"** del cuadro "Árbol de almacenamiento" del
árbol "Controlador:IDE" que aparece vacío.

![Seleccionamos CD](../img/01-virtual-box/01-virtual-box-13.png)

## Buscar archivo

- Pulsamos en el **icono "CD"** de la parte de la derecha.

![Buscar archivo](../img/01-virtual-box/01-virtual-box-14.png)

## Seleccionar ISO

- Buscamos el **archivo ISO de Ubuntu** anteriormente descargado.

![Seleccionar ISO](../img/01-virtual-box/01-virtual-box-15.png)

## Cerrar configuración

- Si todo ha salido bien nos aparecerá el **ISO en la configuración**.

![Cerrar configuración](../img/01-virtual-box/01-virtual-box-16.png)

## Finalizar

- Si todo ha salido bien nos aparecerá la **máquina con la ISO** en VirtualBox.

![Listar Máquina Virtual](../img/01-virtual-box/01-virtual-box-17.png)




# Intalar Ubuntu




## Iniciar Máquina Virtual

- Pulsamos sobre el icono de "**Iniciar**", y el sistema empieza a cargarse.

![Inicia Máquina Virtual](../img/01-virtual-box/01-ubuntu-04.png)

## Seleccionar idioma

- Seleccionamos "**Español**" y pulsamos en "**Instalar Ubuntu**".

![Seleccionar idioma](../img/01-virtual-box/01-ubuntu-05.png)

## Descagas opcionales

- Podemos seleccionar ciertas **Descargas opcionales**.

![Descagas opcionales](../img/01-virtual-box/01-ubuntu-06.png)

## Tipo de instalación

- Seleccionamos "**Borrar disco e instalar Ubuntu**".

![Tipo de instalación](../img/01-virtual-box/01-ubuntu-07.png)

## Adevertencia

- Acepamos la advertencia de "**cambios en los discos**"".

![Adevertencia](../img/01-virtual-box/01-ubuntu-08.png)

## Ubicación

- Introducimos "**Madrid**" como ubicación.

![Ubicación](../img/01-virtual-box/01-ubuntu-09.png)

## Teclado

- Seleccionamos el "**tipo de teclado**" de nuestro ordenador.

![Teclado](../img/01-virtual-box/01-ubuntu-10.png)

## Usuario y contraseña

- Introducimos "**Usuario y contraseña**".

![Usuario y contraseña](../img/01-virtual-box/01-ubuntu-11.png)

## Esperar

- Esperamos a que la instalación termine.

![Esperar](../img/01-virtual-box/01-ubuntu-12.png)

## Reiniciar

- Pulsamos en "**Reiniciar ahora**"

![Reiniciar](../img/01-virtual-box/01-ubuntu-13.png)

## Pulsar ENTER

- Pulsamos "**ENTER**" para finalizar.

![Pulsar ENTER](../img/01-virtual-box/01-ubuntu-14.png)

## Cargar Ubuntu

- Después del último paso se **carga Ubuntu**.

![Cargar Ubuntu](../img/01-virtual-box/01-ubuntu-15.png)

## Apagar Ubuntu

- Pulsamos en el botón situado en la **parte superior derecha**.

![Apagar Ubuntu](../img/01-virtual-box/01-ubuntu-16.png)

## Finalizar

- Aparece una ventana y pulsamos "**Apagar**"

![Finalizar](../img/01-virtual-box/01-ubuntu-17.png)

## Rearancar

- La próxima vez que queramos ejecutar el sistema pusaremos en "**Iniciar**".

![Listar Máquina Virtual](../img/01-virtual-box/01-virtual-box-18.png)




# Importar Máquina Virtual




## ¿Qué es eso?

- Podemos **importar máquinas** anteriormente creadas.

## Importar VDI

- Creamos una máquina virtual igual que antes, pero al crear el Disco Virtual seleccionamos el **archivo VDI**.

![Importar VDI](../img/01-virtual-box/01-virtual-box-18.png)

## Importar OVF

- Pulsamos en "**Archivo > Importar servicio virtualizado...**" y seleccionamos el archivo OVF.

![Importar OVF](../img/01-virtual-box/01-virtual-box-19.png)

## Exportar OVF

- Para ello pulsamos en "**Archivo > Exportar servicio virtualizado...**" y seguimos las instrucciones.

![Exportar OVF](../img/01-virtual-box/01-virtual-box-19.png)
