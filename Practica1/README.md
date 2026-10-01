# Diseños y requisitos

Antes de comenzar con la configuración, se han definido los siguientes requisitos y decisiones.

## Dominios ficticios

Los dos dominios elegidos son:

* **apachedocs.local** → para el servidor Apache.
* **nginxdocs.local** → para el servidor Nginx.

Se han elegido estos nombres porque identifican fácilmente el servidor al que hacen referencia. La extensión **`.local`** indica que se trata de dominios utilizados en un entorno de pruebas local.

## Puerto interno de Apache

Apache escuchará en el puerto interno **8080**.

Nginx será la única puerta de entrada desde el exterior mediante los puertos **80 y 443**, y se encargará de enviar las peticiones al servidor Apache por el puerto **8080** dentro de la red Docker.

## MPM de Apache

Se utilizará **`mpm_event`**.

Está pensado para gestionar muchas conexiones al mismo tiempo, utilizando la memoria de forma más eficiente y mejorando el rendimiento del servidor.




