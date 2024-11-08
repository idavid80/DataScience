# Data Visualization with Python

## 📘 Descripción
La visualización de datos es una técnica para presentar datos complejos de manera gráfica y fácil de entender. En el análisis de grandes volúmenes de datos y en la toma de decisiones basadas en datos, la visualización de datos es fundamental. En este módulo, exploraremos qué es la visualización de datos, algunas prácticas recomendadas para crear gráficos y visualizaciones eficaces, y conoceremos Matplotlib, una de las bibliotecas más utilizadas en Python para graficación. Además, trabajaremos con un conjunto de datos de inmigración en Canadá, el cual servirá como base para las prácticas a lo largo del curso.

---

## Indice

1. [**Introducción a las Herramientas de Visualización de Datos**](#1-introducción-a-las-herramientas-de-visualización-de-datos)


2. [**Herramientas de visualización especializadas**](#2-herramientas-de-visualización-especializadas)  


3. [**Herramientas avanzadas de visualización**](#3-herramientas-avanzadas-de-visualización)  


4. [**Cuadro de mandos (Dashboarding Overview)**](#4-model-development)  


5. [**Evaluación y perfeccionamiento del modelo**](#5-evaluación-y-perfeccionamiento-del-modelo)  


6. [**Objetivos prácticos**](#-objetivos)  



---


## 1. Introducción a las Herramientas de Visualización de Datos

### Descripción General
La visualización de datos es el proceso de mostrar información en formatos visuales (como gráficos, mapas, diagramas) para facilitar su análisis y comprensión.

### Importancia y Mejores Prácticas
- **Áreas de Aplicación:** La visualización de datos es fundamental en áreas como los negocios, la ciencia, la salud y las finanzas.
- **Mejores Prácticas:**
  - Elige el tipo de visualización adecuado según los datos.
  - Usa colores y tipografías que faciliten la lectura.
  - Evita el desorden para asegurar claridad e impacto en el mensaje.

### Tipos Comunes de Gráficos
- **Gráfico de Línea:** Muestra tendencias y cambios a lo largo del tiempo, ideal para identificar patrones y fluctuaciones.
- **Gráfico de Barras:** Compara categorías o grupos, facilitando el contraste visual de sus valores.
- **Gráfico de Dispersión:** Explora la relación entre variables, útil para identificar correlaciones o tendencias.
- **Gráfico de Caja (Box Plot):** Muestra la distribución de los datos, destacando la mediana, los cuartiles y los valores atípicos.
- **Histograma:** Ilustra la distribución de los datos dentro de intervalos, ayudando a entender la concentración y forma de los datos.

### Bibliotecas de Visualización de Datos en Python
1. **Matplotlib:** 
   - Biblioteca completa de gráficos con amplias opciones de personalización.
   - Originalmente creada para visualización de EEG/ECoG.
   - Consta de tres capas arquitectónicas principales:
     - **Capa Backend** - Maneja la renderización a diferentes salidas.
     - **Capa Artista** - Contiene todos los elementos dibujados en un gráfico.
     - **Capa de Script** - Facilita la creación de gráficos con comandos de alto nivel.
   - Se integra sin problemas con entornos como Jupyter Notebook.
   - Tiene diferentes backends disponibles para diversas necesidades de renderización.
   - Permite añadir etiquetas y títulos fácilmente con el objeto `plt`.

2. **Gráficos en Pandas:** 
   - Se integra directamente con DataFrames de Pandas para gráficos rápidos.
   - Permite visualizaciones básicas directamente desde los flujos de análisis de datos.

3. **Seaborn:** 
   - Especializado en visualización estadística.
   - Ofrece paletas de colores y estética predeterminada atractiva, ideal para análisis exploratorio de datos.

4. **Folium:** 
   - Crea mapas interactivos y personalizables, valioso para la visualización de datos geoespaciales.

5. **Plotly:** 
   - Biblioteca interactiva compatible con una variedad de gráficos.
   - Incluye características dinámicas como información al pasar el mouse y zoom.

6. **PyWaffle:** 
   - Visualiza representaciones proporcionales usando cuadrículas de cuadrados o rectángulos, ideal para mostrar porcentajes o proporciones.

### Trabajando con Matplotlib en Python
- **Anatomía de un Gráfico:** Se refiere a los diferentes componentes (título, etiquetas, ejes, leyenda) que conforman una representación visual de los datos.
- **Importación de Datos:** Para crear gráficos, primero carga los datos en un DataFrame de Pandas.
- **Creación de un Gráfico de Línea:**
  - Un gráfico de línea conecta puntos de datos con segmentos de línea recta, a menudo usado para mostrar tendencias.
  - Genera un gráfico de línea en Matplotlib especificando `"line"` en el parámetro `kind` de la función `plot()`.

### Jupyter Notebook
- **Jupyter Notebook** es una aplicación de código abierto para crear y compartir documentos, ideal para integrar código, visualizaciones y explicaciones en un solo lugar.

Con estas herramientas y buenas prácticas, puedes crear visualizaciones de datos efectivas y significativas que faciliten la comprensión y el análisis de la información.


### Guía Rápida: Tareas de Preprocesamiento de Datos en Pandas

| Tarea                     | Sintaxis                              | Descripción                                                     | Ejemplo                                      |
|---------------------------|---------------------------------------|-----------------------------------------------------------------|----------------------------------------------|
| **Cargar datos CSV**      | `pd.read_csv('filename.csv')`         | Leer datos desde un archivo CSV en un DataFrame de Pandas.      | `df_can=pd.read_csv('data.csv')`             |
| **Manejo de Valores Nulos** | `df.dropna()`                      | Eliminar filas con valores nulos.                               | `df_can.dropna()`                            |
|                           | `df.fillna(valor)`                    | Llenar valores nulos con un valor especificado.                 | `df_can.fillna(0)`                           |
| **Eliminar Duplicados**   | `df.drop_duplicates()`               | Eliminar filas duplicadas.                                      | `df_can.drop_duplicates()`                   |
| **Renombrar Columnas**    | `df.rename(columns={'viejo': 'nuevo'})` | Renombrar una o más columnas.                                | `df_can.rename(columns={'Age': 'Años'})`     |
| **Seleccionar Columnas**  | `df['nombre_columna']` o `df.nombre_columna` | Seleccionar una columna.                               | `df_can.Age` o `df_can['Age']`              |
|                           | `df[['col1', 'col2']]`               | Seleccionar múltiples columnas.                                 | `df_can[['Nombre', 'Edad']]`                |
| **Filtrar Filas**         | `df[df['columna'] > valor]`          | Filtrar filas según una condición.                              | `df_can[df_can['Edad'] > 30]`               |
| **Aplicar Funciones a Columnas** | `df['columna'].apply(nombre_funcion)` | Aplicar una función para transformar los valores de una columna. | `df_can['Edad'].apply(lambda x: x + 1)` |
| **Crear Nuevas Columnas** | `df['nueva_columna'] = expresión`    | Crear una nueva columna con valores derivados de otras.         | `df_can['Total'] = df_can['Cantidad'] * df_can['Precio']` |
| **Agrupar y Agregar**     | `df.groupby('columna').agg({'col1': 'sum', 'col2': 'mean'})` | Agrupar filas por una columna y aplicar funciones de agregado. | `df_can.groupby('Categoría').agg({'Total': 'mean'})` |
| **Ordenar Filas**         | `df.sort_values('columna', ascending=True/False)` | Ordenar filas según una columna.                               | `df_can.sort_values('Fecha', ascending=True)` |
| **Mostrar Primeras n Filas** | `df.head(n)`                     | Mostrar las primeras n filas del DataFrame.                     | `df_can.head(3)`                             |
| **Mostrar Últimas n Filas** | `df.tail(n)`                      | Mostrar las últimas n filas del DataFrame.                      | `df_can.tail(3)`                             |
| **Comprobar Valores Nulos** | `df.isnull()`                     | Comprobar valores nulos en el DataFrame.                        | `df_can.isnull()`                            |
| **Seleccionar Filas por Índice** | `df.iloc[indice]`           | Seleccionar filas basándose en el índice entero.                | `df_can.iloc[3]`                             |
|                           | `df.iloc[inicio:fin]`                | Seleccionar un rango de filas.                                  | `df_can.iloc[2:5]`                           |
| **Seleccionar Filas por Etiqueta** | `df.loc[etiqueta]`       | Seleccionar filas basadas en nombre de etiqueta/índice.         | `df_can.loc['Etiqueta']`                     |
|                           | `df.loc[inicio:fin]`                 | Seleccionar un rango de etiquetas/índices.                      | `df_can.loc['Edad':'Cantidad']`              |
| **Estadísticas Resumidas** | `df.describe()`                     | Genera estadísticas descriptivas para columnas numéricas.       | `df_can.describe()`                          |

---

### Guía Rápida: Bibliotecas de Visualización de Datos

| Biblioteca    | Propósito Principal                        | Características Clave                              | Lenguaje de Programación | Nivel de Personalización | Capacidades de Dashboard                  | Tipos de Gráficos Posibles                       |
|---------------|-------------------------------------------|---------------------------------------------------|--------------------------|--------------------------|-------------------------------------------|--------------------------------------------------|
| **Matplotlib**| Visualización general                     | Amplia variedad de tipos de gráficos y opciones de personalización. | Python                   | Alto                     | Requiere componentes y personalización adicional | Líneas, dispersión, barras, histogramas, pasteles, box plot, heatmaps, etc. |
| **Pandas**    | Manipulación de datos con funcionalidad gráfica | Fácil de graficar directamente en estructuras de datos de Pandas. | Python                   | Medio                    | Se puede combinar con frameworks web para dashboards | Líneas, dispersión, barras, histogramas, pasteles, box plot, etc. |
| **Seaborn**   | Visualización de datos estadísticos       | Gráficos estadísticos estilizados.                 | Python                   | Medio                    | Puede combinarse con otras bibliotecas para dashboards | Heatmaps, violín, dispersión, barras, conteo, etc. |
| **Plotly**    | Visualización interactiva de datos        | Visualizaciones interactivas basadas en la web.    | Python, R, JavaScript    | Alto                     | El framework Dash se dedica a dashboards interactivos | Líneas, dispersión, barras, pasteles, gráficos 3D, mapas coropléticos, etc. |
| **Folium**    | Visualización de datos geoespaciales      | Mapas interactivos y personalizables.              | Python                   | Medio                    | Se puede integrar con otros frameworks/bibliotecas para dashboards | Mapas coropléticos, puntos, heatmaps, etc. |
| **PyWaffle**  | Gráficos tipo Waffle                      | Gráficos Waffle para representación proporcional.  | Python                   | Bajo                     | Puede combinarse con otras bibliotecas para gráficos tipo Waffle en dashboards | Gráficos Waffle, cuadrados de pastel, gráficos tipo donut, etc. |

---

## 2. Herramientas de visualización especializadas

### Entendiendo Treemaps y Gráficos Dinámicos (Pivot Charts)

#### ¿Qué es un Treemap?
Un treemap es una visualización que muestra datos jerárquicos mediante rectángulos anidados. Cada nivel de la jerarquía se representa con un rectángulo, que a su vez contiene otros rectángulos para los subniveles. Los treemaps son útiles para visualizar grandes conjuntos de datos en los que la estructura jerárquica es esencial, ofreciendo una forma eficiente e intuitiva de mostrar la información.

#### Aplicaciones Comunes de los Treemaps
Los treemaps se utilizan en distintos campos debido a su capacidad para comunicar datos jerárquicos de manera eficaz:

- **Análisis de Negocios**: Composición de ventas por categorías y subcategorías de productos.
- **Finanzas**: Visualización de portafolios de acciones, sectores e industrias.
- **Gestión de Redes y TI**: Representación del uso de sistemas de archivos o redes.
- **Bioinformática**: Visualización de datos biológicos jerárquicos, como taxonomías.
- **Análisis de Tráfico Web**: Estructura de tráfico, donde cada página web se representa con un rectángulo cuyo tamaño refleja el volumen de visitas.

#### Importancia en la Visualización de Datos
- **Eficiencia Espacial**: Permiten visualizar grandes conjuntos de datos en áreas pequeñas.
- **Representación de Jerarquías**: Ofrecen una representación clara de la estructura y la relación cuantitativa entre elementos.
- **Comparación de Tamaños**: Facilitan la comparación de tamaños entre elementos en distintos niveles de la jerarquía.
- **Análisis Visual Rápido**: Los colores y tamaños de los rectángulos facilitan la identificación de patrones y anomalías.


### Visualización de Datos con Python
#### Guía Rápida: Gráficos con Matplotlib usando Pandas

| Tipo de Gráfico       | Descripción                                                                                         | Función en Pandas                | Ejemplo                                                   | Visual |
|-----------------------|-----------------------------------------------------------------------------------------------------|----------------------------------|-----------------------------------------------------------|--------|
| **Gráfico de Línea**  | Muestra tendencias y cambios a lo largo del tiempo                                                  | `DataFrame.plot.line()`          | `df.plot(x='year', y='sales', kind='line')`               |        |
| **Gráfico de Área**   | Muestra series de datos como áreas rellenas, destacando la relación entre ellas                     | `DataFrame.plot.area()`          | `df.plot(kind='area')`                                    |        |
| **Histograma**        | Muestra barras que representan el conteo de datos en cada intervalo/bin                             | `Series.plot.hist()`             | `df['age'].plot(kind='hist', bins=10)`                    |        |
| **Gráfico de Barras** | Visualiza datos usando barras rectangulares                                                         | `DataFrame.plot.bar()`           | `df.plot(kind='bar')`                                     |        |
| **Gráfico de Pastel** | Representa proporciones o porcentajes de un todo en un gráfico circular                             | `Series.plot.pie()`              | `df.plot(x='Category', y='Percentage', kind='pie')`       |        |
| **Gráfico de Caja**   | Muestra la distribución de un conjunto de datos junto con medidas estadísticas clave                | `DataFrame.plot.box()`           | `df_can.plot(kind='box')`                                 |        |
| **Diagrama de Dispersión** | Usa coordenadas para mostrar valores de dos variables                                       | `DataFrame.plot.scatter()`       | `df.plot(x='Height', y='Weight', kind='scatter')`         |        |

---

#### Guía Rápida: Graficando Directamente con Matplotlib

| Tipo de Gráfico       | Descripción                                                                                         | Función en Matplotlib            | Ejemplo                                                   | Visual |
|-----------------------|-----------------------------------------------------------------------------------------------------|----------------------------------|-----------------------------------------------------------|--------|
| **Gráfico de Línea**  | Muestra tendencias y cambios a lo largo del tiempo                                                  | `plt.plot()`                     | `plt.plot(x, y, color='red', linewidth=2)`                |        |
| **Gráfico de Área**   | Muestra series de datos como áreas rellenas                                                         | `plt.fill_between()`             | `plt.fill_between(x, y1, y2, color='blue', alpha=0.5)`    |        |
| **Histograma**        | Muestra barras que representan el conteo de datos en cada intervalo/bin                             | `plt.hist()`                     | `plt.hist(data, bins=10, color='orange', edgecolor='black')` |     |
| **Gráfico de Barras** | Visualiza datos usando barras rectangulares                                                         | `plt.bar()`                      | `plt.bar(x, height, color='green', width=0.5)`            |        |
| **Gráfico de Pastel** | Representa proporciones o porcentajes de un todo en un gráfico circular                             | `plt.pie()`                      | `plt.pie(sizes, labels=labels, colors=colors, explode=explode)` | |
| **Gráfico de Caja**   | Muestra la distribución de un conjunto de datos junto con medidas estadísticas clave                | `plt.boxplot()`                  | `plt.boxplot(data, notch=True)`                           |        |
| **Diagrama de Dispersión** | Usa coordenadas para mostrar valores de dos variables                                       | `plt.scatter()`                  | `plt.scatter(x, y, color='purple', marker='o', s=50)`     |        |
| **Subplots**          | Crea múltiples gráficos en una sola figura                                                          | `plt.subplots()`                 | `fig, axes = plt.subplots(nrows=2, ncols=2)`              |        |
| **Personalización**   | Personaliza el gráfico: agrega etiquetas, título, leyenda, cuadrícula                               | Varias funciones de personalización | `plt.title('Título') plt.xlabel('Etiqueta X') plt.ylabel('Etiqueta Y') plt.legend() plt.grid(True)` | |

---

## 3. Herramientas avanzadas de visualización

### Folium: Una Herramienta para Visualización de Datos Geoespaciales

- **Folium** es una librería de visualización de datos en Python que facilita la visualización de datos geoespaciales.
  
- Con **Folium**, puedes crear mapas de diferentes estilos, como mapas de nivel de calle, mapas de Stamen y más.

- **Folium** permite crear diferentes estilos de mapa utilizando el parámetro `tiles`.

### Trabajando con Mapas en Folium

- Con **Folium**, es fácil agregar marcadores en los mapas.
  
- El parámetro `location` especifica las coordenadas de latitud y longitud del punto central del mapa.

- Los **marcadores** son cruciales para mejorar la interactividad y agregar contexto a los mapas.

- La función `folium.Marker()` permite especificar los parámetros de ubicación.

- El parámetro **popup** proporciona una etiqueta cuando se hace clic en el marcador.

- Los marcadores también se pueden crear utilizando **"feature group"** para agrupar elementos.

### Mapas Coropléticos (Choropleth Maps)

- Un **mapa coroplético** es un mapa temático donde las áreas se sombrean o se representan con patrones en proporción a la medición de una variable estadística.

- Para crear un mapa coroplético en **Folium**, se necesita un archivo **GeoJson** que incluya los datos geoespaciales de la región.

### Mapbox y los Mapas con Folium

- El **Mapbox Bright Tileset** muestra el nombre de cada país cuando se usa en un mapa.


### Guía Rápida: Mapas, Waffle Charts, Nubes de Palabras y Gráficos en Seaborn

| Función                | Descripción                                                                                                      | Sintaxis                                                  | Ejemplo                                                                                                                                               | Visual |
|------------------------|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| **Folium**             |                                                                                                                  |                                                           |                                                                                                                                                       |        |
| **Mapa**               | Crea un objeto de mapa con coordenadas de centro y nivel de zoom especificados.                                  | `folium.Map(location=[lat, lon], zoom_start=n)`           | `world_map = folium.Map()` <br> `canada = folium.Map(location=[56.130, -106.35], zoom_start=4)`                                                      |        |
| **Marcador**           | Agrega un marcador al mapa con ícono personalizado, popup y opciones de tiles.                                   | `folium.Marker(location=[lat, lon], popup='...', tiles='...').add_to(map)` | `folium.Marker(location=[56.130, -106.35], tooltip='Marker', tiles='Stamen Toner').add_to(world_map)`                                               |        |
| **Círculo**            | Añade un círculo al mapa con radio, color y opacidad de relleno especificados.                                  | `folium.features.CircleMarker(location=[lat, lon], radius=n, color='red', fill_opacity=n).add_to(map)` | `folium.features.CircleMarker(location=[56.130, -106.35], radius=1000, color='red', fill_opacity=0.5).add_to(world_map)`                           |        |
| **CoroMapa (Choropleth)** | Genera un mapa coroplético basado en un archivo GeoJSON y una columna de datos especificada.           | `folium.Choropleth(geo_data='ruta/geojson', data=df, columns=['region', 'valor'], key_on='feature.properties.id', fill_color='YlGnBu').add_to(map)` | `world_map.choropleth(geo_data=world_geo, data=df_can, columns=['Country', 'Total'], key_on='feature.properties.name', fill_color='YlOrRd')` |        |
| **PyWaffle**           |                                                                                                                  |                                                           |                                                                                                                                                       |        |
| **Waffle Chart**       | Crea un gráfico de waffle basado en valores y categorías.                                                        | `plt.figure(FigureClass=Waffle, rows=20, columns=30, values=values)` | `plt.figure(FigureClass=Waffle, rows=20, columns=30, values=df_dsn['Total'], cmap_name='tab20', legend={'labels':label, 'loc':'lower left'})`         |        |
| **Leyenda**            | Añade una leyenda al gráfico de waffle.                                                                         | `waffle_chart.legend(loc='upper left', bbox_to_anchor=(1, 1))` |                                                                                                                                                       |        |
| **Título**             | Añade un título al gráfico de waffle.                                                                           | `waffle_chart.set_title('Título del Gráfico de Waffle')`  |                                                                                                                                                       |        |
| **Etiquetas**          | Agrega etiquetas al gráfico de waffle.                                                                          | `waffle_chart.set_labels(['Etiqueta 1', 'Etiqueta 2', ...])` |                                                                                                                                                       |        |
| **WordCloud (Nube de Palabras)** |                                                                                                         |                                                           |                                                                                                                                                       |        |
| **Nube de Palabras**   | Crea un objeto de nube de palabras basado en datos de texto.                                                   | `wordcloud = WordCloud().generate(text_data)`             | `alice_wc = WordCloud(background_color='white', max_words=2000, mask=alice_mask, stopwords=stopwords); alice_wc.generate(alice_novel)`               |        |
| **Generar**            | Genera la nube de palabras basada en los datos de texto.                                                        | `wordcloud.generate(text_data)`                           |                                                                                                                                                       |        |
| **Mostrar**            | Muestra la nube de palabras usando Matplotlib u otras bibliotecas de visualización.                            | `plt.imshow(wordcloud, interpolation='bilinear')`         |                                                                                                                                                       |        |
| **Opciones**           | Configura opciones para la nube de palabras como fuente, colores, máscara y stopwords.                         | `wordcloud = WordCloud(font_path='ruta/fuente', background_color='white', colormap='Blues', mask=mask_image, stopwords=stopwords).generate(text_data)` |       | 
| **Seaborn**            |                                                                                                                  |                                                           |                                                                                                                                                       |        |
| **Gráfico de Barras**  | Crea un gráfico de barras para visualizar la relación entre una variable categórica y una numérica.             | `sns.barplot(x='x_variable', y='y_variable', data=dataframe)` | `sns.barplot(x='Continent', y='Total', data=df_can1)`                                                           |        |
| **Countplot**          | Genera un gráfico de conteo que muestra la frecuencia de cada categoría en una variable categórica.             | `sns.countplot(x='categoria', data=dataframe)`            | `sns.countplot(x='Continent', data=df_can)`                                                                    |        |
| **Regplot**            | Crea un diagrama de dispersión con una línea de regresión para mostrar la relación entre dos variables numéricas. | `sns.regplot(x='x_variable', y='y_variable', data=dataframe)` | `sns.regplot(x='year', y='total', data=df_tot)`                                                                  |        |

---

## 4. Cuadro de mandos

### Creación de Dashboards con Plotly y Dash

### ¿Qué es Plotly?
**Plotly** es una librería de gráficos interactivos para Python (y otros lenguajes como R y JavaScript). Permite crear gráficos dinámicos, visualizaciones y dashboards, y se destaca por su capacidad de generar gráficos interactivos que pueden ser utilizados en navegadores web. Plotly es especialmente útil para la visualización de datos científicos y de negocios debido a su capacidad para crear gráficos complejos como gráficos de líneas, barras, dispersión, mapas, diagramas de calor, entre otros.

### ¿Qué es Dash?
**Dash** es una librería de Python, de código abierto, desarrollada por Plotly que permite crear aplicaciones web interactivas y dashboards sin necesidad de escribir código en JavaScript. Dash está construido sobre Plotly para crear gráficos interactivos, pero además ofrece herramientas para integrar componentes de interfaz de usuario (UI) como botones, menús desplegables, entradas de texto y otros elementos interactivos. Dash es muy útil para crear aplicaciones basadas en datos donde la visualización, el análisis y la interactividad son esenciales.

- Es fácil construir **interfaces gráficas de usuario (GUIs)** utilizando Dash, ya que abstrae todas las tecnologías necesarias para crear las aplicaciones.

### Componentes de Dash
- Dash se compone de dos bibliotecas principales:
  1. **dash_core_components**: Define componentes interactivos de alto nivel, generados con JavaScript, HTML y CSS a través de la biblioteca React.js.
  2. **dash_html_components**: Proporciona un componente para cada etiqueta de HTML.

### Funciones de Retrollamada (Callbacks)
- Una **función de retrollamada (callback)** es una función de Python que se llama automáticamente por Dash cada vez que cambia la propiedad de un componente de entrada.
- El decorador **@app.callback** se utiliza para decorar la función de retrollamada y decirle a Dash que la ejecute cuando haya un cambio en el valor del componente de entrada.

### Parámetros de la Función Callback
- La función callback toma como parámetros componentes de entrada y salida, realizando operaciones para devolver el resultado deseado en el componente de salida.

### Cheat Sheet: Plotly y Dash

| Función                              | Descripción                                              | Sintaxis                                                                 | Ejemplo                                                                                               |
|--------------------------------------|----------------------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| **Plotly Express**                   |                                                          |                                                                       |                                                                                                       |
| **scatter**                          | Crear un gráfico de dispersión                           | `px.scatter(dataframe, x=x_column, y=y_column)`                       | `px.scatter(df, x=age_array, y=income_array)`                                                         |
| **line**                             | Crear un gráfico de líneas                               | `px.line(x=x_column, y=y_column, title='title')`                       | `px.line(x=months_array, y=no_bicycle_sold_array)`                                                   |
| **bar**                              | Crear un gráfico de barras                               | `px.bar(x=x_column, y=y_column, title='title')`                        | `px.bar(x=grade_array, y=score_array, title='Pass Percentage')`                                       |
| **sunburst**                         | Crear un gráfico de tipo sunburst                         | `px.sunburst(dataframe, path=[col1, col2...], values='column', title='title')` | `px.sunburst(data, path=['Month', 'DestStateName'], values='Flights', title='Flight Distribution Hierarchy')` |
| **histogram**                        | Crear un histograma                                     | `px.histogram(x=x, title="title")`                                    | `px.histogram(x=heights_array, title="Distribution of Heights")`                                     |
| **bubble**                           | Crear un gráfico de burbujas                             | `px.scatter(dataframe, x=x, y=y, size=size, title="title")`          | `px.scatter(bub_data, x="City", y="Numberofcrimes", size="Numberofcrimes", hover_name="City", title='Crime Statistics')` |
| **pie**                              | Crear un gráfico de pastel                               | `px.pie(values=x, names=y, title="title")`                            | `px.pie(values=exp_percent, names=house_holdcategories, title='Household Expenditure')`             |
| **Plotly Graph Objects**             |                                                          |                                                                       |                                                                                                       |
| **Scatter**                          | Crear un gráfico de dispersión                           | `go.Scatter(x=x, y=y, mode='markers')`                                | `go.Scatter(x=age_array, y=income_array, mode='markers')`                                             |
| **Crear un gráfico de líneas**       | Crear un gráfico de líneas                               | `go.Scatter(x=x, y=y, mode='lines')`                                  | `go.Bar(x=months_array, y=no_bicycle_sold_array, mode='lines')`                                       |
| **add_trace**                        | Añadir trazas adicionales a una figura existente         | `fig.add_trace(trace_object)`                                          | `fig.add_trace(go.Scatter(x=months_array, y=no_bicycle_sold_array))`                                 |
| **update_layout**                    | Actualizar el diseño de una figura, como el título, etiquetas de los ejes y anotaciones. | `fig.update_layout(layout_object)`                                    | `fig.update_layout(title='Bicycle Sales', xaxis_title='Months', yaxis_title='Number of Bicycles Sold')` |
| **Dash**                             |                                                          |                                                                       |                                                                                                       |
| **dash_core_components.Input**       | Crear un componente de entrada                           | `dcc.Input(value='', type='text')`                                     | `dcc.Input(value='Hello', type='text')`                                                              |
| **dash_core_components.Graph**       | Crear un componente gráfico                              | `dcc.Graph(figure=fig)`                                                | `dcc.Graph(figure=fig)`                                                                                |
| **dash_html_components.Div**         | Crear un elemento div                                    | `html.Div(children=component_list)`                                    | `html.Div(children=[html.H1('Hello Dash'), html.P('Welcome to Dash')])`                               |
| **dash_core_components.Dropdown**    | Crear un componente de menú desplegable                  | `dcc.Dropdown(options=options_list, value=default_value)`              | `dcc.Dropdown(options=[{'label': 'Option 1', 'value': '1'}, {'label': 'Option 2', 'value': '2'}], value='1')` |

### Recursos adicionales Plotly

- [Python dashboarding tools](https://pyviz.org/dashboarding/)
 
- [John Snow's data journalism](https://www.theguardian.com/news/datablog/2013/mar/15/john-snow-cholera-map)

- [Plotly python](https://plotly.com/python/getting-started/)

- [Plotly graph objects with example](https://plotly.com/python/graph-objects/)

- [Plotly express](https://plotly.com/python/plotly-express/)

- [API reference](https://plotly.com/python-api-reference/)

- [Plotly cheatsheet](https://images.plot.ly/plotly-documentation/images/plotly_js_cheat_sheet.pdf)

- [Plotly community](https://www.coursera.org/learn/python-for-data-visualization/supplement/PfZ9k/additional-resources-for-plotly#:~:text=Plotly%20python,Open%2Dsource%20datasets)

- [Open-source datasets](https://www.coursera.org/learn/python-for-data-visualization/supplement/PfZ9k/additional-resources-for-plotly#:~:text=Plotly%20python,Open%2Dsource%20datasets)

- [Blogs relacionados](https://www.coursera.org/learn/python-for-data-visualization/supplement/PfZ9k/additional-resources-for-plotly#:~:text=Plotly%20python,Open%2Dsource%20datasets)

- [Otros recursos útiles](https://www.coursera.org/learn/python-for-data-visualization/supplement/PfZ9k/additional-resources-for-plotly#:~:text=Plotly%20python,Open%2Dsource%20datasets)

### Recursos adicionales Dash

- [Guía completa del usuario de dash](https://dash.plotly.com/)

- [Componentes básicos de Dash](https://dash.plotly.com/dash-core-components)

- [Componentes HTML de Dash](https://dash.plotly.com/dash-html-components)

- [Foro de la comunidad Dash](https://community.plotly.com/c/python/25)

- [Blogs relacionados](https://medium.com/plotly/tagged/dash)

- [Decoradores de Python - realpython.com](https://realpython.com/primer-on-python-decorators/)

- [Decoradores de Python - peps.python.org](https://www.python.org/dev/peps/pep-0318/#current-syntax)

- [Callbacks con ejemplo](https://dash.plotly.com/basic-callbacks)

- [Galería de aplicaciones Dash](https://dash-gallery.plotly.host/Portal/)

- [Componentes de la comunidad Dash](https://www.coursera.org/learn/python-for-data-visualization/supplement/KyQZl/additional-resources-for-interactive-dashboards#:~:text=Python%20decorators%20reference,Dash%20community%20components)



---

## 🎯 Objetivos

1. **Discutir la visualización de datos y su importancia**:
   - Comprender cómo la visualización de datos facilita la interpretación y el análisis de grandes volúmenes de información.
   - Reconocer el papel crucial que juega la visualización en la toma de decisiones basadas en datos.

2. **Descubrir la historia y arquitectura de Matplotlib**:
   - Conocer el origen y la evolución de Matplotlib como herramienta de visualización.
   - Comprender la arquitectura de Matplotlib, incluyendo sus capas (Backend, Artist, y Scripting) y cómo estas capas interactúan para construir gráficos complejos.

3. **Usar Matplotlib para crear gráficos en Jupyter Notebook**:
   - Familiarizarte con el entorno de Jupyter Notebook para graficar, que facilita la creación y visualización de gráficos en un formato interactivo.
   - Aprender los fundamentos de la creación de gráficos básicos con Matplotlib, incluidos los gráficos de líneas, dispersión, barras, y otros.

4. **Explorar el conjunto de datos de inmigración a Canadá**:
   - Trabajar con un conjunto de datos real sobre inmigración a Canadá.
   - Usar el conjunto de datos para aprender a manipular y analizar datos con Pandas.

5. **Identificar los pasos para analizar datos en un DataFrame de Pandas**:
   - Cargar y explorar conjuntos de datos en Pandas.
   - Realizar tareas básicas de manipulación y limpieza de datos, como selección de columnas, filtrado de filas, y manejo de valores faltantes.

6. **Usar Matplotlib para crear gráficos de líneas**:
   - Crear gráficos de líneas para representar datos continuos, como tendencias en el tiempo.
   - Aprender a personalizar gráficos de líneas, ajustando títulos, etiquetas y colores para mejorar la presentación de los datos.

---

