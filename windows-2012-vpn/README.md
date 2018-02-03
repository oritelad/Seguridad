# Windows Server 2012 - VPN

- [1. Configuración de la Máquina Virtual](#1)
- [2. Instalación del Windows Server 2012](#2)
- []()
- []()
- []()
- []()
- []()
- []()
- []()
- []()
- []()
- []()



![](img/000.png)


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

## 3. Configuración de las tarjetas de red

Solo tenemos que ir `cambiar la Configuración de la red`.

![](img/008.png)

- Le cambiamos el nombre a las tarjetas de red para no confundirnos.

![](img/009.png)

### 3.1 Configuración tarjeta de red Externa

Vamos a la tarjeta de red `Externa` y le damos a `propiedades`.

- Tenemos que desactivar todas las casillas menos la de `TCP/IP Versión 4`

![](img/010.png)

Configuramos la dirección IP como los tenemos en la imagen y luego tenemos que ir `opciones avanzadas`

![](img/011.png)

Vamos a la pestaña de `WINS` y configuramos como tenemos en la imagen.

![](img/012.png)


### 3.2 Configuración Tarjeta de Red Interna

Solo tenemos que establecer una IP en la tarjeta de red `Interna`

![](img/013.png)


## 4. Instalación del rol de Remote Access.

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

## 5. Configuración de Enrutamiento y accesso remoto para VPN

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

- 
![](img/034.png)
![](img/035.png)
![](img/036.png)
![](img/037.png)
![](img/038.png)
![](img/039.png)
