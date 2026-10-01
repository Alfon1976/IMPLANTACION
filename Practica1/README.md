# DISEÑOS Y REQUISITOS

Antes de comenzar con la configuración, se han definido las siguientes decisiones:

## Dominios ficticios

Los dos dominios elegidos son:

* **apachedocs.local** → para Apache.
* **nginxdocs.local** → para Nginx.

### ¿Por qué estos nombres?

* **apachedocs.local**: se ha elegido porque identifica al servidor **Apache**. La extensión `.local` indica que se utiliza en una máquina local.
* **nginxdocs.local**: se ha elegido porque identifica al servidor **Nginx**. La extensión `.local` indica que se utiliza en una máquina local.

## Puerto interno de Apache

Apache escuchará en el puerto interno **8080**.

**Nginx será la única puerta de entrada externa**, utilizando los puertos **80 y 443**. Se encargará de recibir las peticiones y reenviarlas al contenedor Apache mediante el puerto **8080**.

## MPM de Apache

Se selecciona **`mpm_event`**.

Está pensado para gestionar muchas conexiones simultáneas, utilizando menos memoria y mejorando el rendimiento del servidor gracias a una gestión más eficiente de las conexiones.




