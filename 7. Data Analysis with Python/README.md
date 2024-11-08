# Data Analysis with Python

## Indice

1. [**Importar Datasets**](#1-importar-datasets)

2. [**Data Wrangling**](#2-data-wrangling)  


3. [**Explorando Data Analysis**](#3-explorando-data-analysis)  


4. [**Model Development**](#4-model-development)  


5. [**Evaluación y perfeccionamiento del modelo**](#5-evaluación-y-perfeccionamiento-del-modelo)  


6. [**Módulo Extra**: SQL Avanzado para Ingenieros de Datos (Honores)](#6-módulo-extra-sql-avanzado-para-ingenieros-de-datos-honores)  


---

## 1. Importar Datasets

### Estructura de los Datos
- Cada línea en un conjunto de datos es una fila, y los valores están separados por comas.
- Para entender los datos, es necesario analizar los atributos de cada columna.

### Bibliotecas de Python
- Las bibliotecas de Python son colecciones de funciones y métodos que facilitan diversas funcionalidades sin necesidad de escribir código desde cero.
- Se dividen en tres categorías: **Cálculo Científico**, **Visualización de Datos** y **Algoritmos de Aprendizaje Automático**.
- Muchas bibliotecas de ciencia de datos están interconectadas. Por ejemplo, **Scikit-learn** está construido sobre **NumPy**, **SciPy** y **Matplotlib**.

### Lectura de Datos con Pandas
- El **formato de los datos** y la **ruta del archivo** son dos factores clave al leer datos con Pandas.
- El método `read_csv` de Pandas puede leer archivos en formato CSV y cargarlos en un **DataFrame**.
  
### Tipos de Datos en Pandas
- Pandas tiene tipos de datos únicos como **object**, **float**, **Int** y **datetime**.
- Utiliza el método `dtype` para verificar el tipo de dato de cada columna; si hay tipos de datos mal clasificados, es posible que se necesite corregirlos manualmente.
- Conocer los tipos de datos correctos ayuda a aplicar funciones de Python adecuadas a cada columna.

### Resumen Estadístico
- El método `describe()` proporciona un resumen estadístico con el conteo, media, desviación estándar, mínimo, máximo y rangos de cuartiles para las columnas numéricas.
- También puedes usar `include='all'` para obtener resúmenes de las columnas de tipo objeto.
- El resumen estadístico ayuda a identificar problemas potenciales, como valores atípicos que necesitan más atención.

### Inspección de Datos
- El método `info()` ofrece una visión general de las primeras y últimas 30 filas del **DataFrame**, útil para una inspección visual rápida.
- Algunos métricos estadísticos pueden devolver "NaN", lo que indica valores faltantes y que el programa no puede calcular estadísticas para ese tipo de dato.

### Conexión a Bases de Datos
- Python puede conectarse a bases de datos a través de código especializado, generalmente escrito en **Jupyter Notebooks**.
- Las **APIs de SQL** y las **APIs de DB de Python** son las más utilizadas para facilitar la interacción entre Python y el **DBMS** (Sistema de Gestión de Bases de Datos).
- Las APIs de SQL se conectan al **DBMS** mediante una o más llamadas a la API, construyen sentencias SQL como cadenas de texto y utilizan las llamadas para enviar las sentencias SQL al **DBMS** y recuperar resultados y estados.

### DB-API en Python
- **DB-API** es el estándar de Python para interactuar con bases de datos relacionales.
- Utiliza objetos de **conexión** para establecer y gestionar conexiones con la base de datos y objetos **cursor** para ejecutar consultas y recorrer los resultados.
- Los métodos del objeto **Conexión** incluyen `cursor()`, `commit()`, `rollback()` y `close()`.

### Buenas Prácticas
- Puedes importar el módulo de la base de datos, usar la API de **Connect** para abrir una conexión, y luego crear un objeto **cursor** para ejecutar consultas y obtener resultados.
- Recuerda siempre cerrar la conexión con la base de datos para liberar recursos.

## 2. Data Wrangling

### Formato de Datos
- El **formato de los datos** es crucial para hacer que los datos de diversas fuentes sean consistentes y comparables.

### Técnicas en Python
- Domina las técnicas en Python para convertir **unidades de medida**, como transformar "millas por galón en ciudad" a "litros por 100 kilómetros en ciudad", para facilitar la comparación y el análisis.

### Identificación y Corrección de Tipos de Datos
- Adquiere habilidades para **identificar y corregir** los tipos de datos en Python, asegurando que los datos estén representados con precisión para posteriores análisis estadísticos.

### Normalización de Datos
- **La normalización de datos** ayuda a hacer que las variables sean comparables y elimina sesgos inherentes en los modelos estadísticos.
- Puedes aplicar **Escalado de Características**, **Min-Max** y **Z-Score** para normalizar datos y aplicar cada técnica en Python utilizando los métodos de pandas.

### Binning
- **Binning** es un método de preprocesamiento de datos para mejorar la precisión del modelo y la visualización de datos.
- Ejecute técnicas de **binning** en Python utilizando el método "linspace" de **numpy** y el método "cut" de **pandas**, especialmente para variables numéricas como "precio".

### Visualización de Datos
- Utiliza **histogramas** para visualizar la distribución de los datos agrupados (binned) y obtener información sobre la distribución de características.

### Variables Categóricas y Modelos Estadísticos
- Los modelos estadísticos generalmente requieren **entradas numéricas**, lo que hace necesario convertir **variables categóricas**, como "tipo de combustible", a formatos numéricos.
- Puedes implementar la técnica de **one-hot encoding** en Python utilizando el método `get_dummies` de pandas para transformar las variables categóricas en un formato adecuado para modelos de aprendizaje automático.

## 3. Explorando Data Analysis

### Funciones Estadísticas Básicas en Pandas
- Herramientas como la función **'describe'** en pandas pueden calcular rápidamente medidas estadísticas clave, como la **media**, **desviación estándar** y **cuartiles** para todas las variables numéricas en tu DataFrame.

### Resumen de Datos Categóricos
- Utiliza la función **'value_counts'** para resumir los datos en diferentes categorías para variables categóricas.

### Visualización de Distribución de Datos
- **Diagramas de caja (Box plots)** ofrecen una representación visual de la distribución de los datos para variables numéricas, mostrando características como la **mediana**, los **cuartiles** y los **valores atípicos (outliers)**.

### Relación entre Variables Continuas
- **Diagramas de dispersión (Scatter plots)** son excelentes para explorar relaciones entre variables continuas, como el **tamaño del motor** y el **precio** en un conjunto de datos de automóviles.

### Relación entre Variables Categóricas
- Utiliza el método **'groupby'** de pandas para explorar relaciones entre variables categóricas.

### Visualización Avanzada
- Utiliza **tablas dinámicas (pivot tables)** y **mapas de calor (heat maps)** para obtener mejores visualizaciones de los datos.

### Correlación entre Variables
- La **correlación** entre variables es una medida estadística que indica cómo los cambios en una variable pueden estar asociados con los cambios en otra variable.

### Visualización de Correlación
- Al explorar la correlación, utiliza **diagramas de dispersión** combinados con una **línea de regresión** para visualizar las relaciones entre variables.
- Las funciones de visualización como **regplot** de la librería **seaborn** son especialmente útiles para explorar la correlación.

### Correlación de Pearson
- **La correlación de Pearson** es un método clave para evaluar la correlación entre variables numéricas continuas. Proporciona dos valores importantes:
  - El **coeficiente** que indica la fuerza y la dirección de la correlación.
  - El **valor p (P-value)** que evalúa la certeza de la correlación.
  
- Un coeficiente de correlación cercano a **1** o **-1** indica una fuerte correlación positiva o negativa, respectivamente, mientras que un valor cercano a **0** sugiere que no hay correlación.

- Para los valores p, los valores menores a **0.001** indican una fuerte certeza en la correlación, mientras que valores mayores indican menor certeza. Ambos, el coeficiente y el valor p, son importantes para confirmar una correlación fuerte.

### Mapas de Calor
- Los **mapas de calor (heatmaps)** proporcionan un resumen visual completo de la fuerza y la dirección de las correlaciones entre varias variables.


### Hoja de Referencia: Análisis Exploratorio de Datos con Python

| Paquete/Método                    | Descripción                                                                 | Ejemplo de Código                                                               |
|-----------------------------------|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **Correlación del dataframe completo**   | Matriz de correlación creada utilizando todos los atributos del conjunto de datos. | `df.corr()`                                                                     |
| **Correlación de atributos específicos**  | Matriz de correlación creada utilizando atributos específicos del conjunto de datos. | `df[['atributo1','atributo2',...]].corr()`                                      |
| **Gráfico de dispersión**           | Crea un gráfico de dispersión utilizando los puntos de datos de la variable dependiente en el eje x y la variable independiente en el eje y. | `from matplotlib import pyplot as plt`<br> `plt.scatter(df[['atributo_1']], df[['atributo_2']])` |
| **Gráfico de regresión**           | Utiliza las variables dependientes e independientes en un DataFrame de Pandas para crear un gráfico de dispersión con una línea de regresión lineal generada para los datos. | `import seaborn as sns`<br> `sns.regplot(x='atributo_1', y='atributo_2', data=df)` |
| **Gráfico de caja**                | Crea un gráfico de caja (box-and-whisker) utilizando el DataFrame de pandas, la variable dependiente e independiente. | `import seaborn as sns`<br> `sns.boxplot(x='atributo_1', y='atributo_2', data=df)` |
| **Agrupación por atributos**      | Crea un grupo de diferentes atributos de un conjunto de datos para crear un subconjunto de los datos. | `df_group = df[['atributo_1','atributo_2',...]]`                                |
| **Sentencias GroupBy**            | a. Agrupa los datos por diferentes categorías de un atributo, mostrando el valor promedio de los atributos numéricos con la misma categoría.<br>b. Agrupa los datos por diferentes categorías de múltiples atributos, mostrando el valor promedio de los atributos numéricos con la misma categoría. | `a. df_group = df_group.groupby(['atributo_1'],as_index=False).mean()`<br>`b. df_group = df_group.groupby(['atributo_1', 'atributo_2'],as_index=False).mean()` |
| **Tablas dinámicas**              | Crea tablas dinámicas para una mejor representación de los datos en función de los parámetros. | `grouped_pivot = df_group.pivot(index='atributo_1', columns='atributo_2')`     |
| **Gráfico pseudocolor**           | Crea una imagen de mapa de calor utilizando un gráfico pseudocolor (o pcolor) utilizando la tabla dinámica como datos. | `from matplotlib import pyplot as plt`<br> `plt.pcolor(grouped_pivot, cmap='RdBu')` |
| **Coeficiente de Pearson y p-valor** | Calcula el coeficiente de Pearson y el p-valor de un par de atributos. | `from scipy import stats`<br> `pearson_coef, p_value = stats.pearsonr(df['atributo_1'], df['atributo_2'])` |

---

## 4. Model Development

- **Regresión lineal**: Se refiere al uso de una variable independiente para hacer una predicción.

- **Regresión lineal múltiple**: Puedes usar la regresión lineal múltiple para explicar la relación entre una variable objetivo continua **y** y dos o más variables predictoras **x**.

- **Regresión lineal simple (SLR)**: Es un método utilizado para entender la relación entre dos variables: la variable independiente (predictora) **x** y la variable dependiente (objetivo) **y**.

- **Gráficos de regresión y residuos**: Usa las funciones `regplot` y `residplot` de la biblioteca Seaborn para crear gráficos de regresión y residuos, que te ayudan a identificar la fuerza, dirección y linealidad de la relación entre tus variables independientes y dependientes.

- **Evaluación con gráficos de residuos**: Cuando uses gráficos de residuos para la evaluación del modelo, los residuos deben tener un **promedio cercano a cero**, estar distribuidos uniformemente alrededor del eje **x** y tener una **varianza consistente**. Si no se cumplen estas condiciones, considera ajustar tu modelo.

- **Gráficos de distribución para modelos con múltiples características**: Aprende a construir gráficos de distribución para comparar valores predichos y reales, especialmente cuando tu modelo incluye más de una variable independiente. Esto te ayudará a obtener una visión más profunda sobre la precisión de tu modelo a través de diferentes rangos de valores.

- **Regresión polinómica**: El orden de los polinomios afecta el ajuste del modelo a tus datos. Aplica la función `polyfit` de Python para desarrollar modelos de regresión polinómica que se ajusten a tu conjunto de datos específico.

- **Transformación de características**: Para preparar tus datos para un modelado más preciso, utiliza técnicas de transformación de características, en particular con la librería `preprocessing` de **scikit-learn**. Transforma tus datos usando características polinómicas y módulos como `StandardScaler` para normalizar los datos.

- **Pipelines**: Los pipelines te permiten simplificar cómo realizas transformaciones y predicciones de forma secuencial. Puedes usar pipelines en **scikit-learn** para optimizar tu proceso de modelado.

- **Entrenamiento de un pipeline**: Puedes construir y entrenar un pipeline para automatizar tareas como la normalización, la transformación polinómica y la realización de predicciones.

- **Evaluación de modelos**: Para determinar el ajuste de tu modelo, puedes realizar evaluaciones de muestra usando el **Error Cuadrático Medio (MSE)**, utilizando la función `mean_squared_error` de **scikit-learn**, y usar el método `score` para obtener el valor **R-squared**.

- **R-squared y MSE**: Un modelo con un **valor de R-squared** alto cerca de 1 y un **MSE bajo** generalmente es un buen ajuste, mientras que un modelo con un valor bajo de R-squared y un MSE alto puede no ser útil.

- **Sobreajuste**: Presta atención a situaciones en las que tu valor de **R-squared** podría ser negativo, lo que puede indicar un sobreajuste.

- **Evaluación de modelos**: Utiliza tanto visualizaciones como medidas numéricas para comparar diferentes modelos.

- **MSE como medida**: El **Error Cuadrático Medio (MSE)** es quizás la medida numérica más intuitiva para determinar si un modelo es bueno.

- **Gráfico de distribución para regresión lineal múltiple**: Un gráfico de distribución es adecuado para regresión lineal múltiple.

- **Valor aceptable de R-squared**: Un valor de R-squared aceptable depende de lo que estás estudiando y de tu caso de uso.

- **Evaluación del ajuste del modelo**: Para evaluar el ajuste de tu modelo, aplica visualizaciones (como gráficos de regresión y residuos) y medidas numéricas como los coeficientes del modelo para evaluar la sensatez del modelo.

- **Uso de MSE y R-squared**: Utiliza el **Error Cuadrático Medio (MSE)** para medir el promedio de los cuadrados de los errores entre los valores reales y predichos, y examina **R-squared** para entender la proporción de la varianza en la variable dependiente que es predecible a partir de las variables independientes.

- **Análisis de gráficos de residuos**: Los residuos deben estar distribuidos aleatoriamente alrededor de cero para un buen modelo. Un gráfico de residuos curvado o inexactitudes en ciertos rangos sugieren un comportamiento no lineal o la necesidad de más datos.

### Cheat Sheet: Desarrollo de Modelos con Python

| **Proceso**                       | **Descripción**                                                                                                                                                                  | **Ejemplo de Código**                                                                                                           |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| **Regresión Lineal**              | Crea un objeto de modelo de regresión lineal, que se utiliza para predecir una variable continua a partir de una o más variables independientes.                                    | ```python                                                                                                                       from sklearn.linear_model import LinearRegression lr = LinearRegression() ``` |
| **Entrenar el modelo de regresión lineal** | Entrenar el modelo de regresión lineal con los datos seleccionados, separando los atributos de entrada y salida. Si solo hay un atributo de entrada, es regresión lineal simple; si hay varios, es regresión lineal múltiple. | ```python                                                                                                                       X = df[['attribute_1', 'attribute_2']] Y = df['target_attribute'] lr.fit(X, Y) ``` |
| **Generar predicciones de salida** | Predecir el valor de salida para un conjunto de valores de atributos de entrada.                                                                                                    | ```python                                                                                                                       Y_hat = lr.predict(X) ``` |
| **Identificar los coeficientes y el intercepto** | Obtener el valor del coeficiente de pendiente (m) y el valor del intercepto (c) del modelo de regresión lineal.                                                                 | ```python                                                                                                                       coeff = lr.coef_ intercept = lr.intercept_ ``` |
| **Gráfico de residuos**          | Realiza una regresión de y sobre x (puede ser una regresión robusta o polinómica) y luego dibuja un gráfico de dispersión de los residuos.                                         | ```python                                                                                                                       import seaborn as sns sns.residplot(x=df[['attribute_1']], y=df[['target_attribute']]) ``` |
| **Gráfico de distribución**      | Traza la distribución de los datos con respecto a un atributo específico.                                                                                                         | ```python                                                                                                                       import seaborn as sns sns.distplot(df['attribute_name'], hist=False) ``` |
| **Regresión polinómica**         | Utiliza el paquete `numpy` para crear características de una sola variable y ajustar un modelo polinómico a esos datos.                                                             | ```python                                                                                                                       import numpy as np f = np.polyfit(x, y, n) p = np.poly1d(f) Y_hat = p(x) ``` |
| **Regresión Polinómica Multivariable** | Genera una nueva matriz de características que incluye todas las combinaciones polinómicas de los atributos, con un grado menor o igual al especificado.                         | ```python                                                                                                                       from sklearn.preprocessing import PolynomialFeatures Z = df[['attribute_1', 'attribute_2']] pr = PolynomialFeatures(degree=n) Z_pr = pr.fit_transform(Z) ``` |
| **Pipeline**                      | Los pipelines de datos simplifican los pasos de procesamiento de datos. Un pipeline se crea con una lista de tuplas que incluyen el nombre del modelo y su constructor correspondiente. | ```python                                                                                                                       from sklearn.pipeline import Pipeline from sklearn.preprocessing import StandardScaler Input=[('scale', StandardScaler()), ('polynomial', PolynomialFeatures(include_bias=False)), ('model', LinearRegression())] pipe = Pipeline(Input) Z = Z.astype(float) pipe.fit(Z, y) ypipe = pipe.predict(Z) ``` |
| **Valor R^2**                     | El valor R^2 (o coeficiente de determinación) es una medida que indica cuán cerca están los datos de la línea de regresión ajustada. Mide el porcentaje de variación explicado por el modelo. | **a.** ```python X = df[['attribute_1', 'attribute_2']] Y = df['target_attribute'] lr.fit(X, Y) R2_score = lr.score(X, Y) ```<br> **b.** ```python from sklearn.metrics import r2_score f = np.polyfit(x, y, n) p = np.poly1d(f) R2_score = r2_score(y, p(x)) ``` |
| **Valor MSE (Error Cuadrático Medio)** | El Error Cuadrático Medio (MSE) mide el promedio de los cuadrados de los errores, es decir, la diferencia entre los valores reales y los valores estimados.                          | ```python                                                                                                                       from sklearn.metrics import mean_squared_error mse = mean_squared_error(Y, Y_hat) ``` |

## 5. Evaluación y perfeccionamiento del modelo

### Dividir los Datos
- **train_test_split()**: Utilizas este método para dividir tus datos en conjuntos de entrenamiento y prueba. El conjunto de entrenamiento se utiliza para entrenar el modelo, descubrir relaciones predictivas, y luego el conjunto de prueba se usa para evaluar el rendimiento del modelo.

### Error de Generalización
- El **error de generalización** se utiliza para medir qué tan bien tu modelo predice datos no vistos previamente.

### Validación Cruzada
- **Validación cruzada**: Consiste en dividir los datos en **"pliegues"** (folds). Utilizas algunos pliegues como conjunto de entrenamiento y otros como conjunto de prueba. Luego, iteras a través de los pliegues hasta que cada partición sea usada tanto para el entrenamiento como para las pruebas. Al final, se promedia el resultado para estimar el error fuera de la muestra (out-of-sample).

### Selección del Orden Polinómico
- Elige el **mejor orden del polinomio** para ajustar tus datos minimizando el **error de prueba**. Esto se puede hacer comparando el **Error Cuadrático Medio (MSE)** con el orden de los polinomios ajustados en un gráfico.

### Problemas de Sobreajuste y Subajuste
- Los problemas que surgen cuando seleccionas el **orden polinómico incorrecto** incluyen el **sobreajuste (overfitting)** y el **subajuste (underfitting)**. 
  - El **subajuste** ocurre cuando el modelo es demasiado simple para capturar la complejidad de los datos.
  - El **sobreajuste** ocurre cuando el modelo es demasiado complejo y ajusta demasiado bien a los datos de entrenamiento, pero no generaliza bien a los datos de prueba.

### Regresión Ridge
- Utiliza **regresión ridge** cuando existe una **relación fuerte** entre las variables independientes. La **regresión ridge** previene el sobreajuste al controlar la magnitud de los coeficientes polinómicos mediante un **hiperparámetro**, llamado **alpha**.
  
#### Determinación del valor de Alpha:
1. Divide los datos en conjunto de entrenamiento y conjunto de validación.
2. Comienza con un valor pequeño para alpha.
3. Entrena el modelo y realiza predicciones usando los datos de validación.
4. Calcula el valor de **R-squared** y almacena los resultados.
5. Repite el proceso para valores mayores de alpha.
6. Selecciona el valor de alpha que maximice el valor de **R-squared**.

### Búsqueda en Rejilla (Grid Search)
- La **búsqueda en rejilla** te permite explorar múltiples hiperparámetros utilizando la librería **Scikit-learn**. Esta técnica itera sobre los parámetros usando validación cruzada y selecciona los valores óptimos de los hiperparámetros basándose en los resultados.

#### Uso de GridSearchCV:
- **GridSearchCV()** toma un diccionario como argumento donde la **clave** es el nombre del hiperparámetro y los **valores** son los valores de los hiperparámetros que deseas iterar.

```python
from sklearn.model_selection import GridSearchCV

# Ejemplo de uso de GridSearchCV con un diccionario de parámetros
param_grid = {
    'alpha': [0.1, 1, 10, 100],
    'max_iter': [100, 200, 500]
}

# Crear el modelo
model = Ridge()

# Usar GridSearchCV para encontrar el mejor conjunto de hiperparámetros
grid_search = GridSearchCV(estimator=model, param_grid=param_grid, cv=5)
grid_search.fit(X_train, y_train)

# Resultados
print("Mejores parámetros:", grid_search.best_params_)

```

### Cheat Sheet: Evaluación y Refinamiento de Modelos con Python

# Cheat Sheet: Evaluación y Refinamiento de Modelos con Python

| **Proceso**                       | **Descripción**                                                                                                                                                                     | **Ejemplo de Código**                                                                                                           |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| **División de los datos para entrenamiento y prueba** | Este proceso consiste en separar primero el atributo objetivo (lo que queremos predecir) del resto de los datos. Después, dividimos los datos en dos partes: una para entrenar el modelo y otra para probarlo. | ```python                                                                                                                       from sklearn.model_selection import train_test_split y_data = df['target_attribute'] x_data=df.drop('target_attribute',axis=1) x_train, x_test, y_train, y_test = train_test_split(x_data, y_data, test_size=0.10, random_state=1) ``` |
| **Puntaje de validación cruzada** | Si no tienes suficientes datos, se utiliza la validación cruzada. Esto significa que los datos se dividen en varias partes y el modelo se entrena y evalúa varias veces para obtener un rendimiento más fiable. | ```python                                                                                                                       from sklearn.model_selection import cross_val_score from sklearn.linear_model import LinearRegression lre=LinearRegression() Rcross = cross_val_score(lre,x_data[['attribute_1']],y_data,cv=n) Mean = Rcross.mean() Std_dev = Rcross.std() ``` |
| **Predicción con validación cruzada** | Usar un modelo validado a través de validación cruzada para hacer predicciones más precisas sobre los datos de salida. | ```python                                                                                                                       from sklearn.model_selection import cross_val_predict from sklearn.linear_model import LinearRegression lre=LinearRegression() yhat = cross_val_predict(lre,x_data[['attribute_1']], y_data,cv=4) ``` |
| **Regresión Ridge y Predicción** | Para crear un modelo de regresión polinómica que se ajuste mejor a los datos y evite el sobreajuste, se utiliza la regresión Ridge. Esta técnica ajusta el impacto de los parámetros de mayor orden mediante un parámetro llamado *alpha*. | ```python                                                                                                                       from sklearn.linear_model import Ridge pr=PolynomialFeatures(degree=2) x_train_pr=pr.fit_transform(x_train[['attribute_1', 'attribute_2', ...]]) x_test_pr=pr.fit_transform(x_test[['attribute_1', 'attribute_2',...]]) RigeModel=Ridge(alpha=1) RigeModel.fit(x_train_pr, y_train) yhat = RigeModel.predict(x_test_pr) ``` |
| **Búsqueda en cuadrícula (Grid Search)** | Grid Search te ayuda a encontrar el valor adecuado para el parámetro *alpha* que hace que el modelo de regresión Ridge funcione de manera óptima. Además, utiliza validación cruzada para mejorar la precisión del modelo. | ```python                                                                                                                       from sklearn.model_selection import GridSearchCV from sklearn.linear_model import Ridge parameters= [{'alpha': [0.001,0.1,1, 10, 100, 1000, 10000, ...]}] RR=Ridge() Grid1 = GridSearchCV(RR, parameters1,cv=4) Grid1.fit(x_data[['attribute_1', 'attribute_2', ...]], y_data) BestRR=Grid1.best_estimator_ BestRR.score(x_test[['attribute_1', 'attribute_2', ...]], y_test) ``` |

