# Análisis de Datos de Lanzamientos de SpaceX

Este proyecto se enfoca en recopilar y analizar datos de lanzamientos de SpaceX a través de la API REST de SpaceX y mediante técnicas de web scraping. El objetivo es construir un conjunto de datos limpio y estructurado que permita predecir si SpaceX intentará aterrizar un cohete en sus misiones.

## Descripción del Proyecto

Utilizaremos la API de SpaceX para extraer datos detallados sobre los lanzamientos, incluyendo información del cohete, carga útil, especificaciones de lanzamiento, aterrizaje y resultados. Trabajaremos con el endpoint de lanzamientos pasados:

https://api.spacexdata.com/v4/launches/past

### Etapas del Proyecto

1. **Recopilación de datos mediante API**  
   - Realizaremos una solicitud `GET` para obtener datos en formato JSON, que luego transformaremos en un DataFrame utilizando `json_normalize`.
   - Consultaremos endpoints adicionales para recopilar detalles específicos, como el modelo del cohete y la carga útil, almacenándolos en listas para su análisis.

2. **Filtrado de Datos**  
   - Filtraremos los datos de lanzamiento para incluir solo los lanzamientos del Falcon 9, excluyendo aquellos relacionados con el Falcon 1.

3. **Manejo de Nulos**  
   - En la columna `PayloadMass`, reemplazaremos los valores NULL por el promedio calculado de esta columna.
   - En el caso de la columna `LandingPad`, los valores NULL representan lanzamientos sin plataforma de aterrizaje, y serán tratados con técnicas de codificación en caliente más adelante.

4. **Web Scraping de Wikipedia**  
   - Utilizaremos `BeautifulSoup` para extraer datos de tablas HTML relacionadas con los lanzamientos de Falcon 9 en páginas de Wikipedia.
   - Convertiremos estas tablas en DataFrames de Pandas para su análisis.

### Librerías Utilizadas

- `requests` para realizar las solicitudes a la API de SpaceX.
- `pandas` para manipulación de datos.
- `BeautifulSoup` para realizar el web scraping.
