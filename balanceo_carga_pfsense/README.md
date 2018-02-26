# Balanceo de cargas con PfSense
En esta actividad vamos configurar una máquina con PfSense para que actúe como un balanceador de cargas de dos redes con acceso a internet.

# Configuración Máquina Virtual para PfSense.

Tenemos que tener 3 interfaces de red para simular un balanceo de carga con el `PfSense`.

- La primera tarjeta de red en `Adaptador Puente`.

![](img/001.png)

- La segunda tarjeta de red `Interna`.

![](img/002.png)

- La tercera tarjeta de red `Adaptador Puente`

![](img/003.png)

Ya tenemos en la máquina virtual con 3 tarjetas de red.

## Configurar Las tarjeta de red en PfSense.

En la práctica anterior teniamos configurado dos tarjeta de red, por lo tanto solo vamos a configurar la tercera tarjeta de red.

![](img/005.png)

Vamos a configurar para que em0 y em2 sean para el adaptador puente.

![](img/006.png)

em1 como comprobamos es para la LAN Interna.

![](img/007.png)

![](img/008.png)

Ya tenemos las 3 interfaces configuradas.


![](img/010.png)

Configuramos en el Equipo cliente la interfaz de red con la siguiente dirección IP.

![](img/011.png)

Nos conectamos al pfsense desde un navegador.

![](img/012.png)

Entramos al pfsense.

![](img/013.png)

Vamos a System y Routing.

![](img/014.png)

Comprobamos nuestras interfaces.

![](img/015.png)

![](img/016.png)

Ahora vamos a crear un grupo y dentro vamos a meter las dos interfaces para el balanceo de carga.

![](img/017.png)

Lo llamamos balanceo.

![](img/018.png)

Vamos a Firewall y reglas.

![](img/019.png)

Vamos a la interfaz de LAN y le damos editar y vamos a Gateway y seleccionamos el grupo creado.

![](img/020.png)


![](img/021.png)

Comprobamos en Gateway que ahora nuestra puerta de enlace es el grupo de balanceo de carga, es decir las dos interfaces.


![](img/022.png)

Realizamos una comprobación para saber como va su trama.

![](img/023.png)
