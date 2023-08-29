# Informe 1: Instalación de Linux y Herramientas.
Electrónica Digital I.

Grupo 5 Equipo 3.

Rico, Miller - Espinel, Danna.

mricol@unal.edu.co - despinelc@unal.edu.co

##Instalación de Linux.

Descargamos la imagen del sistema operativo linux versión Mint desde la página web oficial https://linuxmint.com/ en este caso elegimos la versión Cinnamon.

Imagen

Descargamos balena etcher para flashear la usb que usaremos como unidad de booteo en el computador.

Imagen Etcher

Imagen Flasheo Etcher

Instalamos limpiamente el sistema operativo en el computador

##Instalación de Herramientas

###Miniconda
Instalamos el paquete de recursos miniconda descargando el instalador desde la página web oficial en la sección de descargas para Linux: https://docs.conda.io/en/latest/miniconda.html#linux-installers

En la terminal, localizamos la carpeta de descargas y ejecutamos el instalador.

###Digital
Descargamos el archivo Digital.zip del repositorio, lo ubicamos en una carpeta de trabajo  y lo extraemos.

Desde la terminal localizamos la carpeta y ejecutamos el programa:

Imagen Digital

###yosys y verilog

Al intentar la primera instalación de las herramientas yosys y verilog falla su instalación, esto debido a la versión de Python:

Imagen Error verilog

Imagen Error yosys

##Método limpio de instalación de herramientas.

Para instalar las herramientas necesarias sin problemas seguimos los siguientes pasos:

1. Actualizamos miniconda en el entorno base con el comando: conda update conda
2. Creamos el entorno digital y establecemos la versión de Python en la 3.10 con el comando: conda create -n digital python=3.10
3. Cambiamos el entorno al digital previamente definido: conda activate digital
4. Una vez en este entorno podemos instalar las herramientas siempre y cuando la versión de Python sea la 3.10, para verificar esto ejecutamos el comando: python --version
5. Instalamos las herramienta gtkwave y graphviz con los comandos: conda install -c conda-forge gtkwave y conda install -c conda-forge graphviz
6. Instalamos las herramientas yosys y verilog con los comandos: conda install -c "litex-hub" yosys y conda install -c "litex-hub" iverilog
7. Verificamos las versiones de yosys y verilog:
8. Instalamos la nueva herramienta netlistsvg con el comando: conda install -c symbiflow netlistsvg



