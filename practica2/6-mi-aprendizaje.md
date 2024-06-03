
# Reflexión sobre los Aprendizajes Logrados

Antes de realizar esta práctica, mis conocimientos sobre Docker y la administración de contenedores eran principalmente teóricos. A través de la práctica, he logrado consolidar y expandir significativamente mi comprensión y habilidades prácticas en varias áreas clave, las cuales detallo a continuación:

### Principales Aprendizajes

1. **Mapeo de Puertos en Docker**: 
   - Aprendí a utilizar el mapeo de puertos de manera efectiva al crear contenedores. Entendí la diferencia entre mapear puertos específicos y dejar que Docker asigne puertos aleatorios automáticamente con el flag `-P`.
   - Practiqué el uso del comando `docker run` con la opción `--publish` para especificar puertos tanto en el host como en el contenedor, lo cual es crucial para permitir la comunicación externa con los servicios ejecutados en los contenedores.

2. **Gestión de Contenedores**:
   - Me familiaricé con los comandos básicos para ejecutar, listar y gestionar contenedores (`docker run`, `docker ps`, `docker rm`, etc.).
   - Aprendí a interactuar con contenedores en ejecución utilizando `docker exec`, incluyendo la ejecución de comandos y la apertura de sesiones shell interactivas dentro de los contenedores.

3. **Operaciones con Jenkins**:
   - Implementé un contenedor de Jenkins y aprendí a acceder a su interfaz web, así como a obtener la contraseña inicial necesaria para la configuración.
   - Ejecuté comandos dentro del contenedor Jenkins y accedí a archivos internos, lo cual es fundamental para la gestión y resolución de problemas en entornos de producción.

4. **Manejo de Variables de Entorno**:
   - Comprendí la importancia de las variables de entorno para configurar aplicaciones de manera flexible y segura.
   - Practiqué la creación de contenedores con variables de entorno tanto directamente en la línea de comandos como mediante archivos `.env`.

5. **Trabajo con Redes en Docker**:
   - Aprendí a crear y gestionar redes personalizadas en Docker, permitiendo la segmentación y organización de contenedores en diferentes subredes.
   - Implementé y vinculé contenedores a redes específicas, lo cual es esencial para construir arquitecturas de aplicaciones más complejas y seguras.

6. **Persistencia de Datos**:
   - Experimenté con la persistencia de datos en contenedores de bases de datos (MySQL y PostgreSQL). Aprendí que los datos pueden mantenerse intactos si el contenedor de la base de datos no se elimina, lo cual es fundamental para la recuperación y continuidad del negocio.

### Documentación de Problemas Solucionados

- **Problema con la Ejecución de Comandos en Jenkins**:
  Al intentar ejecutar comandos interactivos dentro del contenedor Jenkins, inicialmente no obtenía la salida esperada. Esto se debió a no haber especificado correctamente los flags `-i` y `-t`. Aprendí que para ejecutar comandos interactivos con salida visible, es crucial utilizar `docker exec -it`.

- **Persistencia de Datos en WordPress**:
  Al eliminar y recrear el contenedor de WordPress, observé que la configuración y las publicaciones no se perdieron porque los datos estaban almacenados en la base de datos MySQL. Esto subraya la importancia de separar los datos persistentes de los contenedores efímeros para mantener la integridad de la información.

Estos aprendizajes y soluciones prácticas han enriquecido significativamente mi formación profesional, permitiéndome abordar con mayor confianza la implementación y administración de aplicaciones en contenedores.
