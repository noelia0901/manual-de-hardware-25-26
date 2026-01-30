# Índice


1. [Introducción](#introducción)
2. [Preparación de la máquina virtual](#preparación-de-la-máquina-virtual)
3. [Instalación](#instalación)<br>
a. [Idioma](#idioma)<br>
b. [Configuración del sistema](#configuración-del-sistema)<br>
c. [Particionado del disco](##particionado-del-disco)<br>
d. [Últimos detalles](#últimos-detalles)<br>
4. [Conclusión](#conclusión)
5. [Enlaces](#enlaces)


# Introducción


En esta práctica se va a instalar un SO Kali Linux en una máquina virtual desde cero. La página oficial ofrece una paquete ya preparado para su uso en máquinas virtuales, pero en esta ocasión se va a hacer de cero. Pero primero, ¿Qué es Kali?


Kali Linux es una distribución de Linux enfocada en seguridad informática y pruebas de penetración (pentesting). Está basada en Debian y ya cuenta con todas las herramientas necesarias para analizar, auditar y probar la seguridad de redes, sistemas y aplicaciones. Es un sistema pensado para laboratorios, prácticas de seguridad y pentesting.


Esta práctica se va a realizar utilizando virtualbox.


# Preparación de la máquina virtual


Antes de instalar Kali, se ha de preparar la máquina virtual. Para ello, se va a crear una nueva máquina a la que en mi caso he nombrado Kali. A esta se añade la ISO descargada de la web oficial. Las especificaciones de la máquina que he elegido son las siguientes: <br>
**Base Memory**: Por defecto (Fig. 1)<br>
**Numbers of CPU**: 2 (Fig.1)<br>
**Disco duro**: por defecto 25 GB (Fig.2)<br>


![Ajustes meemoria base y CPU](./img/2.png)
***Fig 1. Ajustes memoria base y CPU***


![Ajustes disco duro](./img/3.png)
***Fig 2. Ajustes disco duro***


Tras esto le damos a aceptar y antes de encender la máquina le damos a configuración->experto y configuramos:<br>
**General**: Features-> Portapapeles compartido y drag-and-drop-> Bidireccional (fig. 3). Esto nos permite copiar y pegar desde nuestro ordenador anfitrión y viceversa.<br>
**Red**: Habilitar adaptador puente. (fig.4)<br>


![Ajustes generales](./img/4.png)
***Fig 3. Ajustes generales***


![Ajustes de red](./img/5.png)
***Fig 4. Ajustes de red***


# Instalación


Una vez que ya tenemos todos los ajustes hechos, iniciamos la máquina y le damos a la primera opción de Graphical install. (fig. 5)
![Pantalla inicio insalación](./img/6.png)
***Fig 5. Pantalla de instalación de inicio***


## Idioma
Ahora nos pide la configuración del idioma para el SO, la ubicación y la distribución del teclado. He seleccionado **Español -> España -> Español** (fig. 6,7 y 8.)
![Selección de idioma](./img/7.png)
***Fig 6. Selección de idioma***


![Selección de pais](./img/9.png)
***Fig 7. Selección de país***


![Configuración de teclado](./img/10.png)
***Fig 8. Configuración de teclado***




## Configuración del sistema


Tras indicar el idioma, va a pedir que nombremos como queremos que se llame la máquina y si le damos a continuar, nos va a pedir nombre de dominio. En mi caso, no he puesto nada (fig.10).
![Nombre de la máquina](./img/11.png)
***Fig 9. Configuración del nombre de la máquina***


![Nombre del dominio](./img/12.png)
***Fig 10. Configuración del nombre del dominio***


Ahora se van a configurar los usuarios y contraseñas. Primero nos va a pedir nuestro nombre (fig. 11), luego el nombre de usuario (fig. 12) y por último la contraseña (fig. 13). <br><br>
![Configuración de nombre](./img/13.png)
***Fig 11. Configuración de nombre***


![Configuración de usuario](./img/14.png)
***Fig 12. Configuración de usuario***


![Configuración de contraseña](./img/15.png)
***Fig 13. Configuración de contraseña***


Por último, nos va a pedir la configuración del reloj. (fig.14)<br><br>


![Configuración del reloj](./img/16.png)
***Fig 14. Configuración del reloj***


## Particionado del disco


Para el particionado del disco, que es la siguiente pantalla, se va a utilizar el *Guiado- utilizar todo el disco*-> *SCSI3(0,0,0)(sda)* como se puede ver en las figuras 15 y 16. Luego se va a escoger *todos los ficheros en una partición*(fig.17), se va a *Finalizar el particionado y escribir los cambios en el disco*-> confirmamos dando a *Sí* (Fig. 18 y 19).




![Método de particionado](./img/17.png)
***Fig 15. Elección del método de particionado***


![Disco a particionar](./img/18.png)
***Fig 16. Elección del disco a particionar***


![Esquema de particionado](./img/19.png)
***Fig 17. Elección del esquema de particionado***


![Finalizar](./img/20.png)
***Fig 18. Finalizar el particionado***


![Confirmar cambios](./img/21.png)
***Fig 19. Confirmación de los cambios***


## Últimos detalles


Para finalizar nos va a pedir que seleccionemos los programas que queremos instalar y yo lo he dejado por defecto (fig 20). Por último nos pide que instalemos GRUB para el arranque y le he dado que *Sí*-> y que lo instale en */dec/sda* como se puede ver en las figuras 21 y 22. Por último terminamos la instalación (fig. 23) y nos permite iniciar Kali tras introducir el usuario y la contraseña (fig. 24 y 25).


![Software a instalar](./img/22.png)
***Fig 20. Elección del software a instalar*** <br>


![Instalación de GRUB](./img/23.png)
***Fig 21. Instalación de GRUB***<br>


![Dispositivo donde se va a instalar](./img/24.png)
***Fig 22. Ubicación donde se va a instalar GRUB***<br>


![Finalización de la instalación](./img/25.png)
***Fig 23. Finalización de la instalación***


![Panatalla de inicio de Kali](./img/26.png)
***Fig 24. Pantalla de inicio de Kali***


![Escritorio](./img/27.png)
***Fig 25. Imagen del escritorio***


# Conclusión


La instalación de Kali es sencilla e intuitiva. Es un gran SO que nos integra muchas de las herramientas utilizadas en la seguridad informática.


# Enlaces
<a href="https://www.kali.org/get-kali/#kali-installer-images">Enlace a la imágenes de Kali de la web oficial</a>