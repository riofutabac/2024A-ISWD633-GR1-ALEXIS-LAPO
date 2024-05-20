# Aprendizajes en Docker

## Gestión de Contenedores

Antes de abordar la práctica,no tenia un conocimiento sobre la creación y gestión de contenedores Docker, pero al realizar la tarea, reforcé algunos conceptos clave y aprendí nuevas formas de abordar problemas comunes.

- Aprendí la importancia de verificar la existencia de contenedores con nombres específicos antes de crear uno nuevo, para evitar conflictos.
- Reforcé el conocimiento sobre cómo detener y eliminar contenedores con comandos como `docker stop` y `docker rm`.
- Me familiaricé con el uso de comandos adicionales como `docker ps -a` para listar todos los contenedores, incluso aquellos que están detenidos.

## Mapeo de Puertos

- Aprendí sobre la importancia y la utilidad del mapeo de puertos en Docker para exponer servicios dentro de un contenedor a la red externa.
- Reforcé mi comprensión sobre cómo usar el parámetro `-p` para especificar mapeos de puertos al crear un contenedor.

## Solución de Problemas

### Eliminar un contenedor con el mismo nombre

Si necesitas eliminar un contenedor con el mismo nombre antes de crear uno nuevo, puedes seguir estos pasos:

```
docker stop <nombre_contenedor>
docker rm <nombre_contenedor>
```

### Eliminar un contenedor en ejecución

Si necesitas eliminar un contenedor que está en ejecución, puedes utilizar el flag `-f` con el comando `docker rm` para forzar su eliminación, incluso si está corriendo:
```
docker rm -f <nombre_contenedor>
```


