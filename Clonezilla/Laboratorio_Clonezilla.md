# Introducción
En este laboratorio se va trabajar con clonezilla. Esta es una herramienta de clonación y copia de seguridad de discos y sistemas completos. Nos sirve para clonar discos o particiones, crear imágenes de sistemas para backup completo y para restaurar sistemas como estaban en el caso de errores. Se ejecuta desde un USB o una ISO por lo que no tiene que estar instalado en el sistema. Este laboratorio sirve como una guía para su uso.


# Preparación del laboratorio
Se va a preparar la máquina para realizar la práctica. Para ello, se descarga y se añade la ISO de clonezilla a la máquina virtual. En este caso voy a utilizar una máquina con un ubuntu server instalado. También se le añade otro disco duro virtual donde se va a realizar la copia.


![Imagen de la configuración de almacenamiento](./img/1.png) </br>
**Imagen sobre la configuración del almacenamiento de la MV**


Para que Clonezilla arranque correctamente tenemos que decirle a la máquina que arranque desde el disco antes que desde el disco duro en sistema→ placa base→ boot device order (BIO only).


![Imagen de la configuración de sistema](./img/2.png) </br>
**Imagen sobre la configuración del sistema de la MV**


En red además añadimos el adaptador puente.


![Imagen sobre la configuración de red](./img/3.png) </br>
**Imagen sobre la configuración de la red de la MV**


# Configuración del clonezilla para la copia de seguridad
Ahora se van a mostrar los pasos a seguir para configurar Clonezilla.
1. Una vez se enciende la máquina, en vez de arrancar el sistema operativo nos arranca el Clonezilla y sale la siguiente pestaña. Le damos a la primera opción. Clonezilla live (VGA 800x600).


![Imagen de la página de inicio de Clonezilla](./img/4.png)


2. Ahora seleccionamos el idioma con el que queremos trabajar. En este caso el español.


![Imagen de la elección del idioma](./img/5.png)


3. Mantenemos la opción por defecto.


![opción por defecto](./img/6.png)


4. Le damos a start Clonezilla.


![Imagen de startClonezilla](./img/7.png)


5.En esta práctica se va a seleccionar la segunda opción de disco a disco. Aunque en un entorno real se haría la primera ‘device-image’.


![Eleción del tipo de copia](./img/8.png)


6. Seleccionamos el modo principiante


![pantallazo modo principiante](./img/9.png)


7. Le damos ahora a la primera opción de local disk a disco local clonado


![pantallazo de opción a disco local](./img/10.png)


8. Ahora escogemos el disco de origen. En este caso el sda.


![Elección disco de origen](./img/11.png)


9. Después escogemos el disco en el que se van a volcar los, en este caso el sdb. Se ha de tener en cuenta de que todo lo que se va a volcar va a borrar los datos del disco de destino.


![Elección disco de destino](./img/12.png)


10. Se da en la primera opción de omitir la comprobación de errores ya que todo funciona correctamente.


![Comprobación de errores](./img/13.png)


11. Seleccionamos la opción por defecto ya que queremos mantener las particiones.


![Mantener particiones](./img/14.png)


12. En este caso es para copiar los ficheros de los log y ambas opciones están bien.


![Opciones de log](./img/15.png)


13. Elegimos la primera que significa que elegimos al final del proceso si apagar, reiniciar, etc.


![Opciones de qué hacer tras el proceso](./img/16.png)


14. Aceptamos que se sobreescriban los discos.


![opciones al iniciarse](./img/18.png)


Ya se está realizando la copia como se ve en los pasos siguientes. Cuando acaba el proceso nos pregunta qué hacer, y yo en este caso apagué la máquina.
![Captura del proceso](./img/19.png)
![Captura de las opciones del final](./img/20.png)




# Comprobación de la copia


Para comprobar que todo ha salido correctamente, basta con mirar el almacenamiento de los discos y ver que el tamaño de ambos sea muy similar. Como se ve en las siguientes imágenes.


![Disco 1 origen](./img/21.png)
![Disco 2 destino](./img/22.png)



