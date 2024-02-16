# Imagenes Docker

> Paula Fernández Suárez

[TOC]

## Definición

Las redes en Docker son una herramienta que se encarga de definir cómo se comunicarán los contenedores de la plataforma entre sí, definiendo donde no está restringida la comunicación entre los contenedores de la misma.

Cada red está asociada con una interfaz puente en el host y se definen reglas de cortafuegos para filtrar el tráfico entre estas interfaces.

## Tipos

### Red Bridge

Los contenedores creados por el usuario son por defecto bridge, y suelen exponer algún puerto utilizando la opción `-p` par amapear puertos.

Nos permite aislar los conteneodres de las diferentes subredes y del exterior y publicar los servicios mediante redirecciones.

#### Redes definidas por el usuario


#### Red bridge por defecto

### Red host

Este tipo de red hace que el anfitrión ofezca el servicio configurado en el puerto de la red del anfitrión, por lo que no tiene IP propia sino que usa la del anfitrión y hace que los revicios sean accesibles directamente desde este.

### Red none

No configura ninguna IP para el contenedor y mo tiene un acceso externo a la red ni a otros contenedores. Tiene la dirección loopback y se utiliza para ejecutar trabajos por lotes.

## Ejemplos

### Despliegue de la aplicación Guestbook

```bash
docker network create red_gestbook
```
![comando_01.png](./images/ejemplo_01/comando_01.png)
```bash
docker run -d --name redis --network red_guestbook redis
```
![comando_02.png](./images/ejemplo_01/comando_02.png)
```bash
docker run -d -p 80:5000 --name guestbook --network red_guestbook iesgn/guestbook
```
![comando_03.png](./images/ejemplo_01/comando_03.png)

Abrimos el navegador para comprobar si se ha ejecutado correctamente el contenedor.
![resultado.png](./images/ejemplo_01/resultado.png)

### Despliegue de la aplicación temperaturas

### Despliegue de Wordpress + mariadb

### Despliegue de tomcat + nginx