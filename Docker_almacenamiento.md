# Docker- Volúmenes y Bind mount

[TOC]

![](.\Docker_almacenamiento\contenedores.png)

## Volúmenes

1. Crea un volumen docker que se llame `miweb`.
   ```shell
   ```

   

2. Crea un contenedor desde la imagen `php:7.4-apache` donde montes en el directorio `/var/www/html` (que sabemos que es el *DocumentRoot* del servidor que nos ofrece esa imagen) el volumen docker que has creado. 
   ```shell
   ```

   

3. Utiliza el comando `docker cp` para copiar un fichero `index.html` en el directorio `/var/www/html`. 
   ```shell
   ```

   

4. Accede al contenedor desde el navegador para ver la información ofrecida por el fichero `index.html`.
   ```shell
   ```

   

5. Borra el contenedor 
   ```shell
   ```

   

6. Crea un nuevo contenedor y monta el mismo volumen como en el ejercicio anterior. 
   ```shell
   ```

   

7. Accede al contenedor desde el navegador para ver la información ofrecida por el fichero `index.html`. ¿Seguía existiendo ese fichero?
   ```shell
   ```

   

## Bind mount

1. Crea un directorio en tu host y dentro crea un fichero `index.html` . 
   ```shell
   ```

   

2. Crea un contenedor desde la imagen `php:7.4-apache` donde montes en el directorio `/var/www/html` el directorio que has creado por medio de `bind mount`. 
   ```shell
   ```

   

3. Accede al contenedor desde el navegador para ver la información ofrecida por el fichero `index.html`. 
   ```shell
   ```

   

4. Modifica el contenido del fichero `index.html` en tu host y comprueba que al refrescar la página ofrecida por el contenedor, el contenido ha cambiado. 
   ```shell
   ```

   

5. Borra el contenedor 
   ```shell
   ```

   

6. Crea un nuevo contenedor y monta el mismo directorio como en el ejercicio anterior. 
   ```shell
   ```

   

7. Accede al contenedor desde el navegador para ver la información ofrecida por el fichero `index.html`. ¿Se sigue viendo el mismo contenido?
   ```shell
   ```

   