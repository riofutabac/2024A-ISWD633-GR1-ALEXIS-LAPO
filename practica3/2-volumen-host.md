# VOLUMEN TIPO HOST
Un volumen host (o bind mount) es un tipo de volumen donde se monta un directorio o archivo específico del sistema de archivos del host en un contenedor.

```
docker run -d --name <nombre contenedor> -v <ruta carpeta host>:<ruta carpeta contenedor> <imagen> 
```

### Crear un volumen tipo host con la imagen nginx:alpine, para la ruta carpeta host: directorio en donde se encuentra la carpeta html en tu computador y para la ruta carpeta contenedor: /usr/share/nginx/html esta ruta se obtiene al revisar la se obtiene desde la documentación
![Volúmenes](imagenes/volumen-host.PNG)

```
docker run -d --name mi-nginx -v /mi/directorio/html:/usr/share/nginx/html nginx:alpine
```
### ¿Qué sucede al ingresar al servidor de nginx?

Al ingresar al servidor de nginx se mostrará el contenido del archivo index.html que se encuentra en la carpeta especificada en el host, en este caso /mi/directorio/html. Si modificas este archivo en el host, los cambios se reflejarán directamente en el servidor.
### ¿Qué pasa con el archivo index.html del contenedor?

El archivo index.html original en el contenedor es reemplazado por el montaje del volumen host. Cualquier archivo en la ruta /usr/share/nginx/html del contenedor será ocultado y remplazado por los archivos del directorio del host.
### Ir a https://html5up.net/ y descargar un template gratuito, descomprirlo dentro de nginx/html
### ¿Qué sucede al ingresar al servidor de nginx?

Al ingresar al servidor de nginx después de descomprimir un template en la carpeta /mi/directorio/html, verás que el servidor refleja el nuevo contenido HTML del template. Esto permite actualizar fácilmente el sitio web sin necesidad de reconstruir o reiniciar el contenedor.
### Eliminar el contenedor

```
docker rm -fv mi-nginx
```
### ¿Qué sucede al crear nuevamente el mismo contenedor con volumen de tipo host a los directorios definidos anteriormente?

Al crear nuevamente el contenedor con el mismo volumen de tipo host, los datos persistirán y el servidor de nginx seguirá mostrando el contenido actual de la carpeta del host. Esto demuestra cómo los volúmenes permiten la persistencia de datos incluso cuando los contenedores son eliminados y recreados.
### ¿Qué hace el comando pwd?
El comando pwd (print working directory) muestra el directorio actual en el que te encuentras en la línea de comandos. Es útil para asegurarte de que estás trabajando en el directorio correcto, especialmente cuando configuras volúmenes en Docker.

Si quieres incluir el comando pwd dentro de un comando de Docker, lo puedes hacer de diferentes maneras dependiendo del shell que estés utilizando.


### Volumen tipo host usando PWD y PowerShell
```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v ${PWD}/<ruta relativa>:<ruta absoluta> <nombre imagen>:<tag> 
```

### Volumen tipo host usando PWD (Git Bash)

```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v $(pwd -W)/html:/usr/share/nginx/html <nombre imagen>:<tag> 
```

### Volumen tipo host usando PWD (en Linux)

```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> -v $(pwd)/html:/usr/share/nginx/html <nombre imagen>:<tag> 
```

