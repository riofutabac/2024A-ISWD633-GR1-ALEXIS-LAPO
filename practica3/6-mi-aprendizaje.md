
## Comparación de Conocimientos Antes y Después de la Práctica

### Antes de la Práctica
Mis conocimientos sobre Docker eran principalmente teóricos, con escasa experiencia práctica en la implementación de entornos completos.

### Principales Aprendizajes y Beneficios para mi Formación Profesional

1. **Redes Docker:**
   - **Antes:** Tenía un conocimiento básico de las redes Docker.
   - **Después:** Aprendí a crear redes personalizadas (`docker network create`) y conectar contenedores a estas redes, mejorando la comunicación interna entre servicios.

2. **Volúmenes en Docker:**
   - **Antes:** Sabía de manera superficial cómo usar volúmenes en Docker.
   - **Después:** Desarrollé habilidades para crear y gestionar volúmenes nombrados (`docker volume create`) y bind mounts, asegurando la persistencia de datos incluso tras la eliminación y recreación de contenedores. Comprendí la importancia de la persistencia de datos y cómo los volúmenes facilitan la portabilidad y flexibilidad de las aplicaciones Docker.

3. **Implementación de Servicios:**
   - **Antes:** Conocía los conceptos básicos de configuración de servicios.
   - **Después:** Configuré un entorno completo con PostgreSQL y Drupal, usando variables de entorno para asegurar el correcto funcionamiento de los servicios.

4. **Administración de Bases de Datos:**
   - **Antes:** Tenía conocimientos limitados sobre la administración de bases de datos en contenedores.
   - **Después:** Utilicé pgAdmin para administrar PostgreSQL, conectándome a través del nombre del contenedor, lo que facilitó la gestión y resolución de problemas de conexión.

5. **Persistencia de Datos:**
   - **Antes:** Sabía que la persistencia de datos era importante, pero no cómo implementarla efectivamente.
   - **Después:** Implementé soluciones de persistencia para PostgreSQL y Drupal, garantizando la continuidad de los datos y configuraciones a pesar de la recreación de contenedores.

### Resolución de Problemas
Durante la práctica, enfrenté un problema de conexión con pgAdmin, que solucioné utilizando el nombre del contenedor (`server-postgres`) en lugar de la dirección IP. Esto destacó la importancia de los nombres de contenedor en redes Docker personalizadas. También tuve problemas con los permisos de las carpetas en el contenedor de Drupal, que solucioné con la ayuda de mi profesora, aprendiendo así la importancia de la gestión de permisos.

### Beneficio para la Formación Profesional
Este ejercicio práctico ha mejorado significativamente mis habilidades técnicas en Docker, esenciales para la ingeniería de software moderna. La capacidad de implementar y gestionar entornos de desarrollo y producción con Docker es altamente valorada en la industria, preparándome mejor para enfrentar desafíos reales en el desarrollo de software y en infraestructura de TI. Esta experiencia práctica fortalece mi base teórica y me proporciona una ventaja competitiva en el ámbito profesional, especialmente en la implementación de soluciones containerizadas y la gestión de datos persistentes.
