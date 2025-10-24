# Instalación de la máquina cliente de Ubuntu



[TOC]



## 1. Requerimientos hardware

Para comenzar buscamos en la página de https://ubuntu.com/download que tipo de sistema operativo queremos descargar. En nuestro caso será Ubuntu Desktop 

<img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-09%20a%20las%2012.05.19.png" alt="Captura de pantalla 2025-10-09 a las 12.05.19" style="zoom:67%;" />

En la propia página también te explica que requerimientos para el hardware se necesitan. Esto lo usaremos como guía para crear nuestra maquina virtual.

<img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-09%20a%20las%2010.42.19.png" alt="Captura de pantalla 2025-10-09 a las 10.42.19" style="zoom:67%;" />

## 2. Configuración de ubicaciones

Para no saturar nuestro equipo, crearemos una carpeta en nuestra unidad de `disco local C` una carpeta para albergar todo lo referente a las máquinas virtuales.

Ruta:

`disco local C > usuarios > creamos una carpeta maquina virtual Ubuntu`



<img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-09%20a%20las%2012.42.32.png" alt="Captura de pantalla 2025-10-09 a las 12.42.32" style="zoom:67%;" />

En mi caso como lo estoy haciendo desde mi ordenador en mi casa la ruta para mi es diferente.

`Disco local C > usuarios > Cris > VirtualBox VMs > UbuntuDesktop`

<img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-09%20a%20las%2013.03.29.png" alt="Captura de pantalla 2025-10-09 a las 13.03.29" style="zoom:67%;" />



## 3. Creación de una máquina virtual Ubuntu

Abrimos Virtual Box y hacemos click en `nueva.` y comenzamos con la configuración.

**Nombre y sitema operativo:**

<img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-09%20a%20las%2012.48.52.png" alt="Captura de pantalla 2025-10-09 a las 12.48.52" style="zoom:50%;" />

- Marcamos la opcion de `omitir instalacion desatendida`

  

**Hardware:**

<img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-09%20a%20las%2012.52.24.png" alt="Captura de pantalla 2025-10-09 a las 12.52.24" style="zoom:67%;" />

**Disco Duro:**

<img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-09%20a%20las%2012.54.40.png" alt="Captura de pantalla 2025-10-09 a las 12.54.40" style="zoom:67%;" />

## 4. Otras configuraciónes 

- Deshabilitar audio.

  <img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-09%20a%20las%2013.05.37.png" alt="Captura de pantalla 2025-10-09 a las 13.05.37" style="zoom:67%;" />

  

- Escogemos red Nat para el adaptador.

![image-20250922171727760](./instalacionDeLaMaquinaClienteUbuntu.assets/image-20250922171727760.png)



## 5. Instalación de Ubuntu desktop

Primero debemos arrancar nuestra máquina virtual, una vez hecho esto nos saldra ya una ventana que nos idica si queremos intentar instalar Ubuntu, presionamos aceptar y comenzamos a instalar seguin los pasos que nos van indicando.

<img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-13%20a%20las%2017.47.26.png" alt="Captura de pantalla 2025-10-13 a las 17.47.26" style="zoom:67%;" />

- Accesibilidad en Ubuntu : no ponemos nada.

- Eleccion de indioma de teclado: Español

  <img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-13%20a%20las%2017.51.47.png" alt="Captura de pantalla 2025-10-13 a las 17.51.47" style="zoom:67%;" />

  

- Conectarse a internet: Utilizar conexión por cable.

- Queremos instalar Ubuntu: si

  <img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-13%20a%20las%2017.54.25.png" alt="Captura de pantalla 2025-10-13 a las 17.54.25" style="zoom:67%;" />

  

- Instalacion interactiva: si.

- Aplicaciones a instalar: Selcción predeterminada.

- ¿Como quieres instalar Ubuntu?:  borrar disco e instalar Ubuntu.

  <img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-13%20a%20las%2018.04.20.png" alt="Captura de pantalla 2025-10-13 a las 18.04.20" style="zoom:67%;" />

  

- Crear cuenta

  

  <img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-13%20a%20las%2018.05.43.png" alt="Captura de pantalla 2025-10-13 a las 18.05.43" style="zoom:67%;" />

  

- Huso horario : Gijon (Asturias, Spain)

  

  Aqui empezará la instalacion de todo lo que hemos ido configurando. Esto tarda unos minutos. Una vez que ha terminado nos pied reiniciar.

  <img src="./instalacionDeLaMaquinaClienteUbuntu.assets/Captura%20de%20pantalla%202025-10-13%20a%20las%2018.34.31.png" alt="Captura de pantalla 2025-10-13 a las 18.34.31" style="zoom:67%;" />

  

## 6. Instalar Guest additions

Son un conjunto de drivrs y utilidades que se instalan dentro del sitema operativo invitado para mejorar la integracion con el sistema anfitrión.

Usos:

- Pantalla completa y resolucion dinámica.

- Portapapeles Bidireccional.

- Arrastrar y soltar archivos.

- Mejor rendimiento gráfico y de ratón.

- Carpetas compartidas.

  

En la ventana de la máquina virtual nos vamos a `Dispositivos > Instalar imagen de CD de las Guest Additions`

Clicamos en el CD que nos aparece y después a `Ejecutar programa` y nos saldra el siguiente mensaje:

![image-20250925163844964](./instalacionDeLaMaquinaClienteUbuntu.assets/image-20250925163844964.png)



Nos pide la autenticación.

![image-20250925163927345](./instalacionDeLaMaquinaClienteUbuntu.assets/image-20250925163927345.png)

Cuando nos disponemos a instalar nos sale un error porque nos falta instalar `bzip2 tar`. Abrimos una nueva terminal y ejecutamos el siguiente comando: `sudo apt install bzip2 tar`.

Ahora si podemos volver a ejecutar las guests additions y seguir con la instalación.

![image-20250925163957807](./instalacionDeLaMaquinaClienteUbuntu.assets/image-20250925163957807.png)

> Si por alguna razón con los pasos anteriores no se instalan las guests additions se pùede hacer directamente desde la consola con `sudo apt install virtualbox-guest-utils`
>
> <img src="./instalacionDeLaMaquinaClienteUbuntu.assets/image-20250925164252343.png" alt="image-20250925164252343" style="zoom:67%;" />
>
> <img src="./instalacionDeLaMaquinaClienteUbuntu.assets/image-20250925164520001.png" alt="image-20250925164520001" style="zoom:67%;" />

Una vez que hemos instalado esto es bueno actualizar el sitema para ello abrimos una nueva terminal y ejecutamso los siguientes comandos:

`Sudo apt update` : para refrescar la lista de paquetes disponibles.

`Sudo apt upgrade`: para descargar e instalar todas las actualizaciones de software disponibles.



Ejecutamos el comando `whoami` para saber cual es el nombre de usuario efectivo. En este caso es **cristinamuniz**

<img src="./instalacionDeLaMaquinaClienteUbuntu.assets/image-20250925164520001.png" alt="image-20250925164520001" style="zoom:67%;" />

Ejecutamos el comando `sudo usermod -aG vboxsf cristinamuniz` para poder tener carpetas compartidas entre el sistema anfitrión y el invitado

Reiniciamos la máquina para que todo quede instalado correctamente.

## Instalación de filezilla

Es una aplicación de software para transferir archivos entre el ordenador local y un servidor remoto a traves de internet. Se conoce como un cliente FTP.

Usos:

- Administración web: subir archivos  de una página web (HTML, CSS, imágenes, etc.) desde tu PC a un web hosting.
- Copias de seguridad: descargar una copia de los archivos de tu sitio web  desde el servidor a tu ordenador local.
- Gestión de archivos: renombrar, eliminar, mover o cambiar permisos (CHMOD) de archivos y carpetas en el servidor remoto.
- Edición rápida: permite editar archivos de configuración o código directamente en el servidor.

Abrimos el centro de aplicaciones, buscamos el filezilla y lo instalamos

<img src="./instalacionDeLaMaquinaClienteUbuntu.assets/image-20250925165106295.png" alt="image-20250925165106295" style="zoom:67%;" />

