# Windows Server 2012 - VPN


- [1. Configuración de la Máquina Virtual](#1)
- [2. Instalación del Windows Server 2012](#2)
- [3. Configuración de las tarjetas de red](#3)
    - [3.1 Configuración tarjeta de red Externa](#4)
    - [3.2 Configuración Tarjeta de Red Interna](#5)
- [4. Instalación del rol de Remote Access.](#6)
- [5. Configuración de Enrutamiento y accesso remoto para VPN](#7)
- [6. Configuración Equipo Cliente para VPN](#8)



![](img/000.png)


**Roberto Hernández Sanabria**


## 1. Configuración de la Máquina Virtual<a name="1"></a>

Tenemos que agregar una nueva máquina virtual en `VirtualBox`.
Es importante que agregamos dos tarjeta de red.

- Una Tarjeta de Red será `Interna`
- Una Tarjeta de Red será `Externa`

![](img/001.png)

## 2. Instalación del Windows Server 2012.<a name="2"></a>

Solo tenemos que agregar en la máquina virtual la `iso del Windows Server 2012`.

- Seguimos los pasos del asistente de `Windows`.
- Instalación se realizará todo por `defecto`

![](img/002.png)

- Seleccionamos el idioma, en nuestro caso el `Español`

![](img/003.png)

- Seleccionamos la versión con entorno gráfico `GUI`.

![](img/004.png)

- No vamos a realizar ninguna partición al disco duro, lo dejaremos por defecto.

![](img/005.png)

- Esperamos que termine la instalación.

En un momento de la instalación nos pedirá la contraseña para el administrador del sistemas operativo `Windows Server 2012`

![](img/006.png)

Ya tenemos instalado el `Windows Server 2012`

![](img/007.png)

## 3. Configuración de las tarjetas de red<a name="3"></a>

Solo tenemos que ir `cambiar la Configuración de la red`.

![](img/008.png)

- Le cambiamos el nombre a las tarjetas de red para no confundirnos.

![](img/009.png)

### 3.1 Configuración tarjeta de red Externa<a name="4"></a>

Vamos a la tarjeta de red `Externa` y le damos a `propiedades`.

- Tenemos que desactivar todas las casillas menos la de `TCP/IP Versión 4`

![](img/010.png)

Configuramos la dirección IP como los tenemos en la imagen y luego tenemos que ir `opciones avanzadas`

![](img/011.png)

Vamos a la pestaña de `WINS` y configuramos como tenemos en la imagen.

![](img/012.png)


### 3.2 Configuración Tarjeta de Red Interna<a name="5"></a>

Solo tenemos que establecer una IP en la tarjeta de red `Interna`

![](img/013.png)


## 4. Instalación del rol de Remote Access.<a name="6"></a>

Solo tenemos que ir `administrador del sistema -> Agregar nuevo rol`.

![](img/014.png)

- Seleccionamos `acceso remoto`

![](img/015.png)

- Le damos a siguiente.

![](img/016.png)

- Seleccionamos la característica `DirectAccess y VPN(RAS)`

![](img/017.png)

- Le damos siguiente.

![](img/018.png)

- Lo dejamos por defecto y siguiente.

![](img/019.png)

- Le damos instalar.

![](img/020.png)

- Seleccionamos `abrir el asisten para introducción`

![](img/021.png)

- Seleccionamos Implementar solo `VPN`

![](img/022.png)

## 5. Configuración de Enrutamiento y accesso remoto para VPN<a name="7"></a>

Tenemos que darle al botón secundario del ratón y le damos a `configurar y habilitar enrutamiento y acceso remoto`


![](img/023.png)

- Le damos siguiente.

![](img/024.png)

- Seleccionamos la que viene por defecto.

![](img/025.png)

- Marcamos solo `VPN`

![](img/026.png)

- Configuramos la tarjeta de red `Externa` y habilitar seguridad en la interfaz.

![](img/027.png)

- Seleccionamos de un intervalo de direcciones especificado.

![](img/028.png)

- Le damos a nuevo y configuramos el intervalo de de direcciones para `IPv4`

![](img/029.png)

- Configuramos el intervalo.

![](img/030.png)

- Ya lo tenemos configurado y le damos siguiente.

![](img/031.png)

- No, usar enrutamiento y acceso remoto para autenticar las solicitudes de conexiones.

![](img/032.png)

- Le damos a finalizar.

![](img/033.png)

- Aceptar el relevo de mensajes DHCP.

![](img/034.png)

Ya tenemos configurado lo de VPN.


![](img/035.png)

- Seleccionamos `IPv4` y vemos la configuración en la tarjeta de red `Externa`

![](img/036.png)

- Seleccionamos y le damos propiedades.

![](img/037.png)

- Vamos a filtros entrantes y vemos los paquetes.

![](img/038.png)

## 6. Configuración Equipo Cliente para VPN<a name="8"></a>

Vamos a la configuración de red del equipo cliente y establecemos la siguiente dirección IP.

![](img/039.png)

- Vamos a la configuración para establecer la `VPN`

![](img/040.png)

- Seleccionamos el de `VPN`

![](img/041.png)

- Usar mi conexión con `VPN`

![](img/042.png)

- Seleccionamos la de configurar internet mas tarde.

![](img/043.png)

- Escribimos la IP de nuestra `VPN`

![](img/044.png)

- Vemos que ya podemos darle a conectar.

![](img/045.png)

- Comprobamos que tenemos agregado la nueva configuración de VPN en la red.

![](img/046.png)

- Le damos con el botón secundario del ratón a propiedades a `VPN` y le indicamos lo siguiente que esta en la foto, en la pestaña de `Seguridad`

![](img/047.png)

- Al darle conectar nos muestra un mensaje. No podemos acceder a la VPN.

![](img/048.png)

- Vamos al servidor y creamos un usuario nuevo llamado `prueba` y le damos a propiedades y le damos a la pestaña `marcado` y le damos a permitir accesso.

![](img/049.png)

- Le damos a conectar desde el equipo cliente a la VPN y ya podemos tener conexión.

![](img/050.png)

- Foto de comprobación que está conectado.

![](img/051.png)

- Realizamos el siguiente comando `ipconfig` para ver si establece conexión a la VPN y nos da la ip de intervalo configurado.

![](img/052.png)
