# Tools for Data Science

Las herramientas se clasifican de la siguiente manera:

## Herramientas de Gestión de Datos
Facilitan el almacenamiento, organización y recuperación de datos. Incluyen bases de datos relacionales, bases de datos NoSQL y plataformas de Big Data.

- **MySQL**: Sistema de gestión de bases de datos relacionales (RDBMS) de código abierto. Utiliza el lenguaje de consulta estructurado (SQL) para gestionar y almacenar datos.
  - Usos comunes: aplicaciones web, almacenes de datos, comercio electrónico.
  
- **PostgreSQL**: Sistema de gestión de bases de datos relacionales (RDBMS) de código abierto. Se destaca por su extensibilidad y cumplimiento de SQL.
  - Características avanzadas: soporte para JSON, búsqueda de texto completo, datos espaciales.
  
- **Apache CouchDB**: Base de datos NoSQL orientada a documentos. Usa JSON para almacenar datos. Es altamente escalable, tolerante a fallos y fácil de usar.

- **MongoDB**: Base de datos NoSQL orientada a documentos. Almacena datos en un formato flexible de JSON y es ideal para aplicaciones web modernas que manejan grandes volúmenes de datos no estructurados.
  - Proporciona escalabilidad, alta disponibilidad y distribución de datos.

- **Apache Cassandra**: Base de datos NoSQL distribuida orientada a documentos, altamente escalable, que puede manejar grandes volúmenes de datos estructurados y no estructurados.
  - Características: alta disponibilidad, tolerancia a fallos, niveles de consistencia ajustables.

- **Hadoop Distributed File System (HDFS)**: Diseñado para trabajar con grandes conjuntos de datos en un entorno de computación distribuida. Procesamiento de datos de alta capacidad mediante la división de archivos en bloques.

- **Ceph**: Plataforma de almacenamiento definida por software, de código abierto, adecuada para entornos de nube híbrida y centros de datos modernos.

- **Elasticsearch**: Motor de búsqueda y herramienta de análisis distribuida. Basada en la biblioteca Lucene, permite búsqueda de texto completo y análisis de datos en tiempo real.

## Herramientas de Integración y Transformación de Datos
Simplifican los pipelines de datos y automatizan los flujos de trabajo de procesamiento de datos.

- **Apache Airflow**: Plataforma de código abierto para autorizar, programar y monitorear flujos de trabajo de datos. Permite definir y ejecutar flujos de trabajo complejos.
  
- **Kubeflow**: Kit de herramientas de código abierto para ejecutar pipelines de ciencia de datos sobre Kubernetes, soporta entrenamiento distribuido y ajuste de hiperparámetros.

- **Apache Kafka**: Plataforma distribuida de streaming para aplicaciones que necesitan publicar, procesar y suscribirse a flujos de registros en tiempo real.

- **Apache NiFi**: Plataforma de integración de datos de código abierto para automatizar el flujo de datos entre sistemas.

- **Apache Spark SQL**: Módulo dentro del ecosistema Spark para trabajar con datos estructurados utilizando SQL y marcos de datos.

## Herramientas de Visualización de Datos
Proporcionan representaciones gráficas de los datos y ayudan a comunicar los conocimientos extraídos.

- **PixieDust**: Biblioteca de código abierto para crear visualizaciones interactivas en Python y cuadernos de Jupyter.
  
- **Hue**: Interfaz web de código abierto para analizar y visualizar grandes conjuntos de datos en Apache Hadoop.

- **Kibana**: Herramienta de visualización de datos que permite interactuar con los datos a través de una interfaz web, comúnmente utilizada con Elasticsearch.

## Herramientas de Despliegue de Modelos
Apoyan en la construcción, despliegue, monitoreo y evaluación de modelos de datos y aprendizaje automático.

- **Apache PredictionIO**: Servidor de aprendizaje automático de código abierto construido sobre una infraestructura escalable y distribuida.
  
- **Kubernetes**: Plataforma de código abierto para orquestación de contenedores, permite gestionar aplicaciones contenidas de manera automática y escalable.

- **Apache Seldon**: Plataforma de código abierto para desplegar y gestionar modelos de aprendizaje automático en Kubernetes.

## Herramientas de Monitoreo y Evaluación de Modelos
Apoyan en la supervisión y evaluación del rendimiento de los modelos desplegados.

- **ModelDB**: Plataforma de código abierto para gestionar modelos de aprendizaje automático y experimentos, permite seguir y reproducir experimentos.

- **Prometheus**: Sistema de monitoreo disponible de forma gratuita, recoge y almacena métricas en tiempo real desde diferentes fuentes.

## Herramientas de Desarrollo y Ejecución de Código
Proporcionan entornos para desarrollar, probar y desplegar código, ofreciendo recursos computacionales para ejecutarlo.

- **Jupyter IDE**: Herramienta de código abierto que soporta lenguajes como Julia, Python y R, permitiendo crear y compartir documentos que contienen código en vivo, ecuaciones y visualizaciones.

- **RStudio**: IDE gratuito y de código abierto diseñado para gestionar y ejecutar código en R.

- **Microsoft Visual Studio**: IDE que soporta varios lenguajes de programación como C, C++, C#, JavaScript, entre otros. 

## Herramientas de Gestión de Activos de Código
Permiten almacenar y gestionar el código, realizar un seguimiento de los cambios y apoyar el desarrollo colaborativo.

- **Git**: Sistema de control de versiones de código abierto para rastrear cambios y colaborar entre desarrolladores.

- **GitHub**: Servicio web para alojar repositorios Git, facilita la colaboración en proyectos de código abierto y la gestión de software.

- **GitLab**: Plataforma web para gestión de repositorios Git, que ofrece integración continua, monitoreo y gestión de proyectos.

- **Bitbucket**: Servicio web para alojamiento de repositorios Git que ofrece características como revisiones de código, solicitudes de extracción y permisos de rama.