# Machine Learning with Python

## Introducción a la Regresión y Evaluación de Modelos

### 1. ¿Qué es la Regresión?
La regresión es una técnica estadística utilizada para predecir valores continuos. En un contexto práctico, la regresión nos permite estimar valores, como la emisión de CO2 de un automóvil, a partir de otras variables relacionadas, como el tamaño del motor o el número de cilindros.

En términos generales, la regresión implica dos tipos de variables:
- **Variable dependiente (Y)**: el valor que deseamos predecir, como la emisión de CO2.
- **Variables independientes (X)**: los valores explicativos, como el tamaño del motor.

En resumen, la regresión busca modelar la relación entre **Y** y una función de **X**. La clave es que **Y** debe ser un valor continuo, mientras que las variables independientes **X** pueden ser categóricas o continuas.

#### Tipos de Regresión
- **Regresión simple**: se utiliza una sola variable independiente. Por ejemplo, predecir la emisión de CO2 en función del tamaño del motor.
- **Regresión múltiple**: se emplean múltiples variables independientes, como tamaño del motor y número de cilindros para estimar la emisión de CO2.

### 2. Aplicaciones Comunes de la Regresión
La regresión se utiliza en diversos campos, como:
- **Ventas**: Previsión de ventas anuales en función de factores como edad, experiencia, etc.
- **Psicología**: Evaluación de la satisfacción individual a partir de factores demográficos.
- **Bienes raíces**: Estimación del precio de una vivienda en función de su tamaño, número de habitaciones, entre otros.

### 3. Introducción a la Regresión Lineal
La regresión lineal es el modelo más básico y común para describir la relación entre dos o más variables. Existen dos tipos principales de modelos:
- **Regresión lineal simple**: una variable independiente (**X**) predice la variable dependiente (**Y**).
- **Regresión lineal múltiple**: varias variables independientes predicen una variable dependiente.

Para aplicar la regresión lineal, necesitamos:
- **Variable independiente (X)**: en este ejemplo, tamaño del motor.
- **Variable dependiente (Y)**: emisión de CO2.

La regresión lineal busca encontrar la mejor línea de ajuste que pase a través de los datos para predecir **Y** a partir de **X**.

### Cómo Funciona la Regresión Lineal
Dado un conjunto de datos, la relación entre la variable independiente (**X**) y la dependiente (**Y**) se representa como:

\[
y = \theta_0 + \theta_1 x
\]

Donde:
- **𝜃₀**: el intercepto (valor de Y cuando X = 0)
- **𝜃₁**: la pendiente de la línea o el coeficiente que determina cómo cambia Y cuando X cambia.

El objetivo es minimizar la suma de errores (diferencia entre los valores observados y los valores predichos), comúnmente representada por el **Error Cuadrático Medio (MSE)**.

#### Ejemplo Práctico
Supongamos que queremos predecir la emisión de CO2 para un coche con un tamaño de motor de 2.4:

Si encontramos:
- **𝜃₀ = 92.94**
- **𝜃₁ = 43.98**

Entonces podemos usar la ecuación de regresión para predecir:

\[
CO₂\ Emission = 92.94 + 43.98 \times 2.4
\]

### 4. Evaluación de Modelos de Regresión
Evaluar el rendimiento del modelo es crucial para determinar su precisión. Hay dos enfoques comunes para la evaluación:

#### 4.1 Entrenar y Probar en el Mismo Conjunto de Datos
Consiste en entrenar el modelo en todo el conjunto de datos y luego probarlo en una porción de ese mismo conjunto. Este método suele dar un alto nivel de precisión en el entrenamiento pero puede llevar a un modelo sobreajustado (alto error en datos desconocidos).

#### 4.2 División de Entrenamiento y Prueba
Aquí, el conjunto de datos se divide en dos subconjuntos:
- **Entrenamiento**: para construir el modelo.
- **Prueba**: para evaluar el rendimiento del modelo en datos no vistos.

Esta técnica es preferida para evaluar la precisión en datos desconocidos, ya que el modelo no ha sido expuesto a los datos de prueba.

#### 4.3 Validación Cruzada K-Fold (K-Fold Cross-Validation)
La validación cruzada K-fold es una técnica avanzada que reduce la variabilidad en los resultados. Aquí, el conjunto de datos se divide en **K subconjuntos** o "folds":
- En cada iteración, uno de los fold se usa como conjunto de prueba, y los restantes como conjunto de entrenamiento.
- Los resultados se promedian para obtener una medida de precisión más estable y confiable.

Este método permite una evaluación más precisa y confiable del rendimiento del modelo.

### Conclusión
La regresión, especialmente la regresión lineal, es una herramienta valiosa para la predicción de valores continuos en múltiples disciplinas. Con una comprensión básica de los principios de ajuste de modelos y técnicas de evaluación, es posible construir y evaluar modelos de regresión robustos.

---

## Introducción a la Clasificación

En este conjunto de apuntes, vamos a explorar los conceptos fundamentales de la clasificación en el ámbito del aprendizaje automático (machine learning). La clasificación es un enfoque de aprendizaje supervisado, lo que significa que se utiliza un conjunto de datos etiquetados (conocidos) para entrenar un modelo que posteriormente sea capaz de predecir o clasificar nuevos casos no etiquetados.

### ¿Qué es la clasificación?

La clasificación consiste en categorizar o clasificar elementos desconocidos en un conjunto discreto de clases. El objetivo es aprender la relación entre un conjunto de variables características y una variable objetivo de interés. Esta variable objetivo en la clasificación es categórica, con valores discretos.

Por ejemplo, si tenemos un conjunto de datos sobre préstamos y sus posibles impagos, la clasificación puede usarse para predecir si un nuevo cliente es un "incumplidor" o "no incumplidor", basándose en características como la edad, ingresos, nivel educativo, etc.

### ¿Cómo funciona la clasificación?

La clasificación funciona al entrenar un modelo con datos etiquetados (conocidos). Una vez que el modelo ha aprendido esta relación, puede usarla para predecir la clase de nuevos datos no etiquetados (por ejemplo, determinar si un nuevo cliente será un incumplidor).

Un buen ejemplo de clasificación es la predicción de impagos de préstamos. Si un banco tiene datos previos de clientes que no pagaron su préstamo, puede usar estos datos para entrenar un clasificador y, cuando un nuevo cliente solicite un préstamo, el banco puede predecir si es un "alto riesgo" o "bajo riesgo".

### Clasificación binaria vs clasificación multiclase

La clasificación puede ser binaria, como en el ejemplo del préstamo (¿incumplidor o no?), o multiclase, como cuando se tienen varias categorías. Un ejemplo de clasificación multiclase es el de predecir a qué grupo de clientes pertenece una persona basándose en datos demográficos (edad, ingresos, etc.). Un banco podría usar este modelo para predecir el grupo de servicio más adecuado para un nuevo cliente: servicio básico, servicio electrónico, servicio Plus o servicio total.

### Casos de uso de la clasificación

La clasificación tiene numerosas aplicaciones en los negocios y en diversas industrias. Algunos ejemplos incluyen:

- **Predicción de cancelaciones**: Identificar si un cliente abandonará el servicio de una empresa (churn detection).
- **Detección de fraude**: Predecir si una transacción es fraudulenta o no.
- **Filtrado de correos electrónicos**: Identificar si un correo es spam o no.
- **Reconocimiento de voz y escritura**: Clasificar el habla o la escritura a mano.

### Algoritmos de clasificación

Existen varios algoritmos de clasificación que se pueden utilizar dependiendo del problema. Algunos de los más comunes son:

- Árboles de decisión
- Naive Bayes
- Análisis discriminante lineal
- K-Vecinos más cercanos (K-Nearest Neighbors, K-NN)
- Regresión logística
- Redes neuronales
- Máquinas de soporte vectorial (SVM)

En este curso, solo cubriremos algunos de estos algoritmos, destacando el de **K-Vecinos más cercanos (K-NN)**.

---

### K-Vecinos más Cercanos (K-NN)

El algoritmo **K-Vecinos más cercanos** es un enfoque popular para la clasificación. Este algoritmo clasifica un punto de datos nuevo según los puntos de datos más cercanos en el conjunto de entrenamiento. 

#### ¿Cómo funciona K-NN?

Imaginemos que una empresa de telecomunicaciones ha segmentado a sus clientes en cuatro grupos según su patrón de uso del servicio. La empresa quiere predecir a qué grupo pertenece un nuevo cliente basándose en su edad e ingresos.

1. **Selección de K**: Se selecciona un valor para K (por ejemplo, 5), que representa la cantidad de vecinos más cercanos que se analizarán.
2. **Cálculo de distancias**: Se calcula la distancia entre el nuevo cliente y los puntos de datos existentes, utilizando una métrica como la distancia **euclidiana**.
3. **Clasificación por mayoría**: Los K vecinos más cercanos al nuevo cliente determinan su clase. Si la mayoría de los K vecinos pertenece a un grupo específico, el nuevo cliente se clasifica en ese grupo.

El valor de **K** es crucial. Si K es muy pequeño, el modelo puede sobreajustarse (overfitting) y si K es muy grande, el modelo puede ser demasiado general (underfitting). Se recomienda probar diferentes valores de K y evaluar cuál da el mejor rendimiento.

#### Elección del valor de K

Elegir el valor correcto de K es esencial. Si seleccionamos un valor bajo, como K=1, el modelo podría ser muy sensible a los datos atípicos o ruido. Por otro lado, si elegimos un valor de K muy alto, el modelo podría volverse demasiado simple y no capturar las complejidades de los datos.

Para encontrar el mejor valor de K, se utiliza la **validación cruzada**, dividiendo los datos en conjuntos de entrenamiento y prueba y evaluando la precisión del modelo con diferentes valores de K.

---

### Métricas de Evaluación para Clasificadores

Las métricas de evaluación son fundamentales para medir el desempeño de un modelo de clasificación. Algunas de las métricas más comunes son:

#### 1. Índice de Jaccard

Mide la similitud entre dos conjuntos de etiquetas (verdaderas y predichas). Se calcula como la intersección de los conjuntos dividido por su unión.

#### 2. Matriz de confusión

Es una herramienta que muestra las predicciones correctas y erróneas en relación con las etiquetas verdaderas. De la matriz se pueden derivar otras métricas, como:

- **Precisión**: Proporción de predicciones correctas entre todas las predicciones hechas.
- **Recuperación**: Proporción de verdaderos positivos entre todos los casos que deberían haber sido positivos.

#### 3. F1-Score

Es la media armónica entre la precisión y la recuperación. Este valor es útil cuando hay un desequilibrio entre las clases.

#### 4. Log-Loss (Pérdida Logarítmica)

Mide el rendimiento de un clasificador cuando el resultado es una probabilidad entre 0 y 1. Cuanto menor sea el valor de log-loss, mejor es el modelo.

---

### Conclusión

La clasificación es una herramienta poderosa en el aprendizaje automático y tiene numerosas aplicaciones en diversas áreas. Los algoritmos como K-NN permiten que los modelos clasifiquen de manera precisa y eficiente, y las métricas de evaluación nos permiten medir y mejorar su desempeño.

---

## Decision Trees

Un **árbol de decisión** es un modelo predictivo utilizado en **clasificación**. Es una estructura de árbol en la que cada nodo interno representa una prueba sobre un atributo, cada rama representa un resultado de la prueba y cada nodo hoja representa una clase o categoría. Se utiliza para predecir el valor de un objetivo basado en características de entrada.

Imagina que eres un investigador médico y necesitas predecir qué medicamento prescribir a un paciente, basándote en sus características, como edad, género, colesterol, etc. Los árboles de decisión pueden ayudarte a tomar esa decisión al clasificar al paciente en una de las categorías, como "Medicamento A" o "Medicamento B".

---

## Cómo Construir un Árbol de Decisión

### 1. **Elegir un Atributo para Dividir los Datos**

El primer paso es seleccionar un atributo para dividir el conjunto de datos. Los atributos pueden ser características como la **edad**, **género**, o **colesterol**. El objetivo es encontrar el atributo más **predictivo** para dividir los datos de manera efectiva.

#### Ejemplo:
Supongamos que tenemos 14 pacientes y decidimos dividir los datos usando el atributo **género**. La división puede ser:
- **Mujeres**: mayor probabilidad de responder al medicamento A.
- **Hombres**: se necesita más información para tomar una decisión.

### 2. **Dividir los Datos y Repetir el Proceso**

Después de hacer una primera división, repetimos el proceso para los subgrupos generados. Cada vez que dividimos los datos, buscamos hacer nodos más **puros** (es decir, nodos donde la mayoría de los casos pertenecen a una sola clase).

---

### Conceptos Clave

#### **Pureza de los Nodos**

Un nodo es **puro** cuando todos los datos en ese nodo pertenecen a la misma clase. El objetivo al construir un árbol de decisión es lograr la mayor pureza posible en los nodos, lo que ayuda a predecir de manera más confiable.

#### **Entropía y Ganancia de Información**

- **Entropía**: Mide el desorden o incertidumbre en los datos. Un nodo con **entropía baja** es más puro, mientras que un nodo con **entropía alta** es más impuro.
- **Ganancia de Información**: Es la cantidad de certeza ganada al dividir los datos. Cuanto mayor sea la ganancia de información, mejor será el atributo seleccionado para la división.

---

### Proceso de Construcción del Árbol

#### 1. **Calcular la Entropía Inicial**
Primero calculamos la entropía de todo el conjunto de datos antes de hacer cualquier división. La fórmula de la entropía nos da una medida de la incertidumbre en los datos. Cuanto más equilibrada esté la distribución entre las clases, mayor será la entropía.

#### 2. **Elegir el Mejor Atributo**
Seleccionamos el atributo que maximice la **ganancia de información**, es decir, el que reduzca más la entropía. Este atributo será el primero en dividir los datos.

**Ejemplo de Cálculo de Entropía:**
Si tenemos 9 pacientes que responden al medicamento B y 5 que responden al medicamento A, la entropía antes de dividir será de 0.94. Luego, calculamos la entropía para cada división posible y seleccionamos la que menor entropía tenga.

#### 3. **Repetir para Cada Rama**
Una vez divididos los datos, repetimos el proceso para cada subgrupo. Evaluamos la entropía en cada subgrupo y seleccionamos el mejor atributo para continuar dividiendo. Esto se hace recursivamente hasta que los nodos sean lo más puros posible.

---

### Ejemplo Práctico: Predicción de Medicamento

Supongamos que tenemos un conjunto de datos con características como **edad**, **género** y **colesterol**. Queremos predecir qué medicamento debe recibir un nuevo paciente. 

1. Dividimos los pacientes por **género**: mujeres tienden a responder mejor al medicamento A, mientras que para los hombres necesitamos más información.
2. Para los hombres, probamos con **colesterol**: si tienen colesterol alto, prescribimos el medicamento A; si es normal, prescribimos el medicamento B.

Este proceso sigue hasta que hemos clasificado a todos los pacientes en uno de los dos grupos (medicamento A o B).

---

### Conclusión

Construir un árbol de decisión consiste en dividir los datos de manera recursiva, seleccionando el atributo más predictivo en cada paso para reducir la impureza de los nodos. A través de este proceso, podemos construir un modelo que prediga con precisión a qué clase pertenece un nuevo caso basado en sus características. 

La **ganancia de información** y la **entropía** son herramientas clave para seleccionar el mejor atributo en cada paso, asegurando que los nodos del árbol sean lo más puros posible para hacer predicciones confiables.


## ¿Qué es la regresión logística?

La **regresión logística** es una técnica estadística y de aprendizaje automático que se utiliza para clasificar registros de un conjunto de datos en función de los valores de los campos de entrada. 

Imaginemos que tenemos un conjunto de datos de telecomunicaciones que nos gustaría analizar para entender qué clientes podrían abandonarnos el próximo mes. Este es un conjunto de datos histórico de clientes, donde cada fila representa a un cliente. Como analistas de esta empresa, necesitamos identificar quiénes se van a marchar y por qué. Usaremos el conjunto de datos para construir un modelo basado en registros históricos y predecir la pérdida futura de clientes.

El conjunto de datos incluye información sobre los servicios que cada cliente ha contratado, detalles de la cuenta del cliente, información demográfica como género y edad, y también información sobre aquellos clientes que han dejado la empresa en el último mes. A esta columna se le llama **churn** (abandono). 

Podemos usar la regresión logística para construir un modelo que prediga el abandono de clientes utilizando las características dadas. En la regresión logística, usamos una o más variables independientes (como la antigüedad, la edad o los ingresos) para predecir un resultado, como el **abandono**, que es nuestra variable dependiente, representando si los clientes dejarán o no el servicio.

### Diferencias con la regresión lineal

La regresión logística es análoga a la **regresión lineal**, pero intenta predecir un campo de destino categórico o discreto, en lugar de uno numérico. En la regresión lineal, podríamos intentar predecir un valor continuo, como el precio de una casa, la presión arterial de un paciente o el consumo de combustible de un coche. Sin embargo, en la regresión logística, predecimos una variable binaria, como "sí/no", "verdadero/falso", "exitoso/no exitoso", "embarazada/no embarazada", etc. Todos estos casos pueden ser codificados como 0 o 1.

Es importante destacar que las variables independientes en regresión logística deben ser continuas. Si son categóricas, deben ser codificadas como variables **dummy** o indicadores, lo que significa transformarlas en valores continuos.

### Aplicaciones de la regresión logística

Dado que la regresión logística es un tipo de algoritmo de clasificación, se puede aplicar en diferentes situaciones. Algunos ejemplos incluyen:

- Predecir la probabilidad de que una persona sufra un ataque al corazón en un período de tiempo determinado, basándonos en su edad, sexo y índice de masa corporal.
- Predecir la probabilidad de mortalidad en un paciente herido.
- Predecir si un paciente tiene una enfermedad como la diabetes, usando características observadas como peso, altura, presión arterial y resultados de diversas pruebas sanguíneas.
- En el contexto del marketing, predecir la probabilidad de que un cliente compre un producto o cancele una suscripción, como hicimos en el ejemplo de **churn**.
- Predecir la probabilidad de fallo de un proceso, sistema o producto.
- Predecir la probabilidad de que un propietario de vivienda incurra en un impago de hipoteca.

En todos estos ejemplos, no solo predecimos la clase de cada caso, sino que también medimos la probabilidad de que un caso pertenezca a una clase específica.

### ¿Cuándo se debe usar regresión logística?

Existen varias situaciones en las que la regresión logística es una buena opción. Aquí presentamos cuatro de ellas:

1. **Cuando el campo objetivo (target) en los datos es categórico, específicamente binario.** Esto puede ser algo como "0/1", "sí/no", "abandono/no abandono", "positivo/negativo", etc.
  
2. **Cuando necesitamos la probabilidad de nuestra predicción.** Por ejemplo, si queremos saber la probabilidad de que un cliente compre un producto. La regresión logística devuelve un puntaje de probabilidad entre 0 y 1 para una muestra de datos. De hecho, la regresión logística predice la probabilidad de esa muestra, y luego asigna la clase discreta a partir de esa probabilidad.

3. **Cuando los datos son linealmente separables.** La frontera de decisión de la regresión logística es una línea, un plano o un hiperplano. Un clasificador clasificará todos los puntos de un lado de la frontera de decisión en una clase y todos los del otro lado en la otra clase. Si tenemos solo dos características y no aplicamos ningún procesamiento polinómico, podemos obtener una desigualdad como \(\theta_0 + \theta_1 x_1 + \theta_2 x_2 > 0\), lo que resulta en un semiplano fácilmente representable gráficamente. Es importante señalar que en la regresión logística también podemos obtener una frontera de decisión compleja utilizando procesamiento polinómico, aunque esto está fuera del alcance de esta explicación.

4. **Cuando necesitamos entender el impacto de una característica.** Puedes seleccionar las mejores características basándote en la significancia estadística de los coeficientes o parámetros del modelo de regresión logística. Es decir, después de encontrar los parámetros óptimos, una característica \(X\) con un peso \(\theta_1\) cercano a cero tiene un efecto menor sobre la predicción en comparación con características con valores absolutos de \(\theta_1\) grandes. Esto nos permite entender el impacto de una variable independiente en la variable dependiente, controlando las demás variables independientes.

### Formalización del problema

Para ilustrar cómo funciona la regresión logística, volvamos a nuestro conjunto de datos. Definimos las variables independientes como **X** y la variable dependiente como **Y**. Para simplificar, podemos codificar los valores del objetivo o dependientes como 0 o 1. El objetivo de la regresión logística es construir un modelo que prediga la clase de cada muestra (en este caso, un cliente), así como la probabilidad de que cada muestra pertenezca a una clase.

Formalmente, tenemos:

- **X** es nuestro conjunto de datos en el espacio de números reales, con **m** dimensiones o características y **n** registros.
- **Y** es la clase que queremos predecir, que puede ser 0 o 1.

Idealmente, un modelo de regresión logística, denotado como \(\hat{Y}\), predice que la clase del cliente es 1, dado sus características **X**. También se puede mostrar fácilmente que la probabilidad de que un cliente pertenezca a la clase 0 puede calcularse como \(1 - P(\text{clase 1})\).

## Diferencia entre regresión lineal y regresión logística

Para entender la regresión logística, es útil primero recordar cómo funciona la regresión lineal. Imaginemos que queremos predecir el ingreso de los clientes de un conjunto de datos. En este caso, la variable independiente podría ser la edad del cliente, y la variable dependiente sería el ingreso, un valor continuo. Con regresión lineal, podemos ajustar una línea o polinomio a los datos y predecir un valor continuo para el ingreso de un cliente en función de su edad.

Sin embargo, si intentamos predecir algo categórico, como la probabilidad de que un cliente abandone la empresa (churn), la regresión lineal no es apropiada. Para ilustrarlo, consideremos el problema de predecir el "churn" de los clientes, con una variable categórica: "churn sí" o "churn no". Si usamos regresión lineal para este caso, el modelo no proporcionaría una probabilidad precisa de que un cliente pertenezca a una de las dos clases.

## El problema con la regresión lineal en clasificación

En un gráfico, si usamos regresión lineal para predecir el "churn" de los clientes, los valores de salida pueden ser cualquier número, como 3 o -2, que no tiene sentido en una clasificación binaria. Para superar este problema, se utiliza un umbral para asignar las predicciones a una de las dos clases. Por ejemplo, si el valor predicho es mayor que 0.5, se asigna a la clase "churn sí" (1); si es menor, a la clase "churn no" (0).

El problema con este enfoque es que la regresión lineal no devuelve probabilidades de forma adecuada. La salida solo nos dice si el cliente pertenece a una clase u otra, pero no cuán probable es que eso ocurra. Además, la función de activación utilizada en la regresión lineal no refleja de manera precisa la probabilidad de un evento.

## Solución: la función sigmoide

Aquí es donde entra la regresión logística. En lugar de usar directamente el valor predicho por la regresión lineal, utilizamos una función matemática llamada **sigmoide**, que transforma el valor continuo en una probabilidad. Esta función es conocida por su forma de "S" y asegura que la salida siempre esté entre 0 y 1, lo que la hace adecuada para interpretar las predicciones como probabilidades.

La fórmula de la función sigmoide es:

\[
\sigma(z) = \frac{1}{1 + e^{-z}}
\]

Donde \( z \) es el valor de la ecuación de regresión lineal. Lo interesante de esta función es que, cuando \( z \) es muy grande, la sigmoide se acerca a 1, lo que significa que la probabilidad de que el cliente pertenezca a la clase "churn sí" es alta. Si \( z \) es muy pequeño, la sigmoide se acerca a 0, lo que indica una baja probabilidad de "churn sí".

## ¿Cómo usamos la regresión logística?

La regresión logística modela la probabilidad de que un punto pertenezca a la clase predicha (por ejemplo, "churn sí"). Matemáticamente, podemos escribirlo como:

\[
P(y=1 \mid x) = \sigma(\theta^T x)
\]

Lo que nos dice es que la probabilidad de que el cliente pertenezca a la clase "churn sí" depende de las características \( x \) del cliente, como su edad e ingresos.

Por ejemplo, si la probabilidad de que un cliente abandone la empresa es del 80% dada su edad e ingresos, la fórmula sería:

\[
P(\text{churn}=1 \mid \text{edad, ingresos}) = 0.8
\]

Y la probabilidad de que el cliente no abandone la empresa sería:

\[
P(\text{churn}=0 \mid \text{edad, ingresos}) = 1 - 0.8 = 0.2
\]

## Entrenamiento de un modelo de regresión logística

El objetivo del entrenamiento de la regresión logística es encontrar los valores adecuados para los parámetros \( \theta \) que minimicen el error en nuestras predicciones. A continuación, describimos los pasos generales para entrenar un modelo de regresión logística:

1. **Inicialización de parámetros**: Comenzamos con valores aleatorios para los parámetros \( \theta \), por ejemplo, \( -1 \) o \( 2 \).
   
2. **Cálculo de la salida del modelo**: Para cada cliente en el conjunto de entrenamiento, calculamos la salida del modelo, que es la probabilidad de que el cliente pertenezca a la clase 1 (por ejemplo, que haga "churn"). Esto se hace usando la función sigmoide sobre el valor de \( \theta^T x \), que es la combinación de los parámetros y las características del cliente.
   
3. **Comparación con el valor real**: Comparamos la salida del modelo con el valor real del cliente. Si el cliente realmente hizo "churn", la salida debería ser cercana a 1; si no hizo "churn", debería ser cercana a 0. Calculamos el error, que es la diferencia entre el valor real y el valor predicho.
   
4. **Cálculo del error total**: Sumamos los errores de todos los clientes en el conjunto de entrenamiento. Esta suma es conocida como la "función de costo", que representa el error total del modelo. El objetivo es minimizar esta función de costo.
   
5. **Actualización de los parámetros**: Usamos un algoritmo de optimización (como el **descenso por gradiente**) para ajustar los parámetros \( \theta \) y reducir el error.

6. **Iteración**: Continuamos el proceso de cálculo y actualización de los parámetros hasta que el modelo tenga un error suficientemente bajo.

## ¿Cómo decidimos cuándo detener el entrenamiento?

Existen diferentes criterios para detener el entrenamiento. Uno de los más comunes es observar la **precisión del modelo**. Si la precisión del modelo es lo suficientemente alta y no mejora significativamente con más iteraciones, detenemos el entrenamiento.

## Conclusión

En resumen, la regresión logística es una técnica poderosa para resolver problemas de clasificación binaria, ya que no solo predice la clase de un punto, sino también la probabilidad de que pertenezca a esa clase. A través del entrenamiento del modelo y el uso de la función sigmoide, podemos construir modelos que no solo predicen correctamente la clase, sino que también nos dan una estimación precisa de la probabilidad asociada con cada predicción.

## Objetivo del Entrenamiento en Regresión Logística

El objetivo principal del entrenamiento en regresión logística es cambiar los parámetros del modelo para que sea la mejor estimación de las etiquetas de las muestras en el conjunto de datos, como por ejemplo, el churn de los clientes. 

¿Cómo hacemos esto? En resumen, primero tenemos que observar la función de costo y ver cuál es la relación entre la función de costo y los parámetros \( \theta \). Entonces, debemos formular la función de costo. Luego, utilizando la derivada de la función de costo, podemos encontrar cómo cambiar los parámetros para reducir el costo o el error.

**Nota importante**: Para entender este proceso, es necesario contar con algunos conocimientos matemáticos básicos. Sin embargo, no te preocupes, ya que la mayoría de los lenguajes de ciencia de datos como Python, R y Scala tienen paquetes o bibliotecas que calculan estos parámetros por ti.

## La Función de Costo

Vamos a ver cómo encontramos la ecuación de la función de costo para un caso de ejemplo. Para hacerlo, podemos usar uno de los clientes del problema de churn.

En general, la ecuación para calcular el costo es la diferencia entre los valores reales de \( y \) y nuestra salida del modelo \( \hat{y} \). Esta es una regla general para la mayoría de las funciones de costo en machine learning. Podemos mostrar esto como el costo de nuestro modelo comparado con las etiquetas reales, lo cual es la diferencia entre el valor predicho por nuestro modelo y el valor real del campo objetivo, donde el valor predicho de nuestro modelo es la sigmoide de \( \theta^T x \).

Por lo general, se usa el cuadrado de esta ecuación debido a la posibilidad de obtener un resultado negativo, y por simplicidad, se considera la mitad de este valor como la función de costo durante el proceso de derivada.

Ahora, podemos escribir la función de costo para todas las muestras en nuestro conjunto de entrenamiento. Por ejemplo, para todos los clientes podemos escribirla como la suma promedio de las funciones de costo de todos los casos. Esta es conocida como el error cuadrático medio y, como es una función de un vector de parámetros \( \theta \), se muestra como \( J(\theta) \).

## Encontrando los Mejores Parámetros

Ahora que tenemos la función de costo, ¿cómo encontramos o establecemos los mejores pesos o parámetros que minimizan esta función de costo? La respuesta es que debemos calcular el punto mínimo de esta función de costo, lo cual nos mostrará los mejores parámetros para nuestro modelo.

Aunque podemos encontrar el punto mínimo de una función utilizando la derivada de la función, no existe una manera fácil de encontrar el mínimo global para una ecuación como esta. Dado que esto es complicado, describir cómo llegar al mínimo global está fuera del alcance de este video.

### Solución: Usar la Función Logaritmo Negativo

La solución es encontrar otra función de costo que tenga el mismo comportamiento pero que sea más fácil de minimizar. 

Para ilustrarlo, recordemos que nuestro modelo es \( \hat{y} \), y nuestro valor real es \( y \), que puede ser 0 o 1. Queremos encontrar una función de costo simple para nuestro modelo. Supongamos que el valor deseado para \( y \) es 1. Esto significa que nuestro modelo es mejor si estima que \( y = 1 \). 

En este caso, necesitamos una función de costo que devuelva 0 si el resultado de nuestro modelo es 1, lo cual coincide con la etiqueta real. La función de costo debe aumentar a medida que el resultado de nuestro modelo se aleja de 1, y debe ser muy grande si el resultado de nuestro modelo se acerca a 0. La función logaritmo negativo proporciona una función de costo como la que necesitamos.

Esto significa que si el valor real es 1 y el modelo también predice 1, la función logaritmo negativo devuelve un costo de 0. Pero si la predicción es menor que 1, la función logaritmo negativo devuelve un costo mayor.

### Función de Costo para Regresión Logística

Así que podemos usar la función logaritmo negativo para calcular el costo de nuestro modelo de regresión logística. Si recordamos, previamente dijimos que generalmente es difícil calcular la derivada de la función de costo. Ahora podemos cambiarla por el logaritmo negativo de nuestro modelo.

Podemos demostrar fácilmente que, si el valor deseado \( y \) es 1, el costo se puede calcular como \( -\log(\hat{y}) \), y si el valor deseado \( y \) es 0, el costo se puede calcular como \( -\log(1 - \hat{y}) \).

Ahora podemos sustituir esto en nuestra función de costo total y reescribirla como esta función. Esta es la función de costo para la regresión logística. Como puedes ver, penaliza situaciones en las que la clase es 0 y la salida del modelo es 1, y viceversa. Recuerda, sin embargo, que \( \hat{y} \) no devuelve una clase como salida, sino un valor entre 0 y 1 que debe ser interpretado como una probabilidad.

## Minimizando la Función de Costo: Usando el Descenso por Gradiente

Ahora podemos usar esta función para encontrar los parámetros de nuestro modelo de tal forma que minimicen el costo. 

**Recapitulando**: Nuestro objetivo era encontrar un modelo que estimara mejor las etiquetas reales. Encontrar el mejor modelo significa encontrar los mejores parámetros \( \theta \) para ese modelo. La primera pregunta era, ¿cómo encontrar los mejores parámetros para nuestro modelo? La respuesta es minimizando la función de costo de nuestro modelo. En otras palabras, para minimizar \( J(\theta) \), acabamos de definir.

### ¿Qué es el Descenso por Gradiente?

La siguiente pregunta es, ¿cómo minimizamos la función de costo? La respuesta es utilizando un enfoque de optimización. Hay diferentes enfoques de optimización, pero usamos uno de los más famosos y efectivos: el **descenso por gradiente**.

El descenso por gradiente es un enfoque iterativo para encontrar el mínimo de una función. Específicamente, en nuestro caso, el descenso por gradiente es una técnica que utiliza la derivada de una función de costo para cambiar los valores de los parámetros y minimizar el costo o error.

### Funcionamiento del Descenso por Gradiente

El objetivo principal del descenso por gradiente es cambiar los valores de los parámetros para minimizar el costo. ¿Cómo puede el descenso por gradiente hacer esto? Imagina que los parámetros o pesos de nuestro modelo están en un espacio bidimensional. Por ejemplo, \( \theta_1 \) y \( \theta_2 \) para dos conjuntos de características, edad e ingresos.

Queremos minimizar la función de costo \( J \), que es una función de las variables \( \theta_1 \) y \( \theta_2 \). Si graficamos la función de costo en función de todos los posibles valores de \( \theta_1 \) y \( \theta_2 \), podemos ver algo como esto:

- Esto representa el valor del error para diferentes valores de los parámetros, es decir, el error en función de los parámetros. A esto se le llama la curva de error o el "cuenco de error" de la función de costo.

Queremos usar este cuenco de error para encontrar los mejores valores de parámetros que minimicen el costo.

### Actualización de Parámetros

Para minimizar el costo, debemos calcular la derivada parcial de la función de costo \( J \) con respecto a cada parámetro en ese punto. Esta derivada nos da la pendiente de la superficie en ese punto y la dirección en la que debemos movernos para reducir el error. Moverse en la dirección opuesta a la pendiente garantiza que descendemos en la curva de error.

Los valores de la derivada también nos indican el tamaño de los pasos a tomar: si la pendiente es grande, tomamos un paso grande, porque estamos lejos del mínimo; si la pendiente es pequeña, tomamos un paso más pequeño.

### El Proceso Iterativo

El descenso por gradiente es un proceso iterativo: en cada iteración, actualizamos los parámetros y minimizamos el costo hasta que el algoritmo converge a un mínimo aceptable.

## Resumen del Algoritmo de Entrenamiento

Recapitulemos lo que hemos hecho hasta ahora, paso a paso:

1. Inicializamos los parámetros con valores aleatorios.
2. Alimentamos la función de costo con el conjunto de entrenamiento y calculamos el costo. Esperamos una tasa de error alta, ya que los parámetros están establecidos aleatoriamente.
3. Calculamos el gradiente de la función de costo utilizando la derivada parcial.
4. Actualizamos los pesos con los nuevos valores de parámetros.
5. Volvemos al paso 2 y alimentamos la función de costo con los nuevos parámetros. Esperamos que el error disminuya.
6. Continuamos este ciclo hasta alcanzar un valor de costo bajo o un número limitado de iteraciones.

Finalmente, después de algunas iteraciones, los parámetros deberían estar aproximadamente ajustados, lo que significa que el modelo está listo para predecir la probabilidad de que un cliente se quede o se vaya.


## Algoritmo de Máquinas de Vectores de Soporte (SVM)

**Support Vector Machine (SVM)**, un algoritmo supervisado utilizado para la **clasificación** de datos, especialmente eficaz en el análisis de datos de alta dimensión.

### 1. ¿Qué es SVM?
- SVM es un algoritmo **supervisado** utilizado para **clasificación**. 
- Se basa en encontrar un **hiperplano** que separe las clases de datos en un espacio de características.
- Inicialmente, los datos son transformados a un espacio de características de mayor dimensión, donde es más fácil separar las clases mediante un hiperplano.
- **Transformación de datos**: Se realiza a través de una técnica llamada **kernel**, que mapea los datos de un espacio de baja dimensión a uno de mayor dimensión, donde los datos se vuelven **linealmente separables**.

### 2. Transformación de los datos (Kernelling)
- **Kernelling** es el proceso de mapear los datos a un espacio de mayor dimensión para hacer que sean linealmente separables.
- Esto se logra mediante una **función kernel** (como lineal, polinómica, RBF o sigmoide), cuya elección depende de los datos y se puede probar experimentalmente.
- **Ejemplo**: Si los datos no son linealmente separables en un espacio 1D, se pueden mapear a un espacio 2D donde la separación se vuelve posible.

### 3. Búsqueda del hiperplano óptimo
- El objetivo de SVM es encontrar el **hiperplano que maximiza la separación entre las dos clases** (mayor margen).
- **Soportes vectores**: Los puntos más cercanos al hiperplano que son los más importantes para determinar la ubicación del hiperplano. Otros puntos no son tan relevantes.
- El proceso de **optimización** busca el hiperplano que maximiza la distancia al **soporte vectorial**, es decir, el margen entre las dos clases.
- Esta optimización se puede resolver con **descenso de gradiente**, aunque los detalles matemáticos no se abordan en este video.

### 4. Clasificación con el hiperplano
- Una vez entrenado el modelo, para **clasificar nuevos puntos**, se utiliza la ecuación del hiperplano.
- Si el resultado de la ecuación es mayor que 0, el punto se clasifica en la clase superior (por encima del hiperplano); si es menor, en la clase inferior (debajo del hiperplano).

### 5. Ventajas y desventajas de SVM

#### Ventajas:
- Es **preciso** en **espacios de alta dimensión**.
- Utiliza solo un subconjunto de los puntos de entrenamiento llamados **soportes vectores**, lo que lo hace **eficiente en memoria**.

#### Desventajas:
- Puede **sobreajustarse** si el número de características es mucho mayor que el número de muestras.
- No proporciona directamente **estimaciones de probabilidad**, lo cual es necesario en muchos problemas de clasificación.
- **No es eficiente** computacionalmente con datasets muy grandes (más de 1,000 muestras).

### 6. ¿Cuándo utilizar SVM?
- **Análisis de imágenes**: clasificación de imágenes, reconocimiento de dígitos manuscritos.
- **Minería de textos**: detección de spam, análisis de sentimientos, clasificación de texto.
- **Clasificación de datos de expresión génica**: debido a la efectividad en datos de alta dimensión.
- También se puede usar en **regresión**, **detección de anomalías** y **agrupamiento**.

En resumen, SVM es un potente algoritmo para clasificación, especialmente cuando se trabaja con datos de alta dimensión, pero tiene algunas limitaciones, especialmente cuando los datos son muy grandes o el sobreajuste es un problema.

---

## Predicción Multiclase: SoftMax, Uno-contra-Todo y Uno-contra-Uno en Clasificación Multiclase

En clasificación multiclase, el objetivo es clasificar datos en múltiples etiquetas de clase. A diferencia de métodos como árboles de decisión o vecinos cercanos, la clasificación multiclase en clasificadores lineales no es tan directa. Podemos extender la regresión logística a una clasificación multiclase usando **regresión SoftMax**, que es una generalización de la regresión logística. Sin embargo, la regresión SoftMax no funciona con máquinas de vectores soporte (SVM); en su lugar, podemos usar los métodos **Uno-contra-Todo** y **Uno-contra-Uno**, que adaptan clasificadores de dos clases para trabajar en problemas multiclase.

### Regresión SoftMax

La regresión SoftMax es similar a la regresión logística, ya que transforma los resultados obtenidos de multiplicar los datos \( x \) con los parámetros \( \theta \) en probabilidades. Para una clasificación de \( K \) clases (0 a \( K-1 \)), se aplica la función SoftMax, que convierte estas distancias en probabilidades usando la fórmula:

\[
\text{softmax}(x, i) = \frac{e^{-\theta_i^T x}}{\sum_{j=1}^{K} e^{-\theta_j^T x}}
\]

El entrenamiento en regresión SoftMax es casi idéntico al de la regresión logística, usando la entropía cruzada. Para hacer predicciones, se calcula la probabilidad de pertenencia a cada clase y se elige la de mayor probabilidad con la función de máximo:

\[
\hat{y} = \text{argmax}_i(\text{softmax}(x, i))
\]

Por ejemplo, para un dato \( x_1 \) y tres clases, podríamos obtener las siguientes probabilidades:

| Clase | Probabilidad |
|-------|--------------|
| 0     | 0.97         |
| 1     | 0.02         |
| 2     | 0.01         |

La predicción sería la clase con mayor probabilidad, en este caso, **clase 0**.

#### Interpretación Geométrica

Cada parámetro \( \theta_i^T x \) representa un hiperplano en el espacio de características. La intersección de estos hiperplanos crea regiones en las que cada región representa una clase. Por ejemplo, una entrada en la región azul se clasificaría como clase 0, una en la región roja como clase 1, y una en la región amarilla como clase 2.

**Nota**: La regresión SoftMax no es compatible con SVM, ya que el entrenamiento en SVM se basa en la maximización del margen y no en la entropía cruzada.

### Uno-contra-Todo (One-vs-Rest)

En el método Uno-contra-Todo, si hay \( K \) clases, se crean \( K \) clasificadores binarios. Para cada clasificador, los ejemplos de la clase de interés se mantienen como están, y los ejemplos de las demás clases se agrupan en una "clase dummy". Así, cada clasificador aprende a diferenciar su clase de interés contra el resto.

Para hacer una predicción, se ignoran las "clases dummy" y se selecciona la clase que obtuvo el mayor valor en su clasificador correspondiente.

#### Problema de Ambigüedad en Uno-contra-Todo

En algunas áreas de espacio, varios clasificadores pueden dar respuestas conflictivas. Para mitigar estas regiones ambiguas, se pueden usar reglas de combinación (como elegir la clase con el puntaje más alto) o considerar la probabilidad de pertenencia real de cada muestra.

### Uno-contra-Uno (One-vs-One)

En el método Uno-contra-Uno, se entrena un clasificador binario para cada par de clases posibles. Por ejemplo, si hay clases 0, 1 y 2, se entrena un clasificador para distinguir entre 0 y 1, otro para 0 y 2, y uno más para 1 y 2. 

Para \( K \) clases, este método requiere \( K(K-1)/2 \) clasificadores binarios. Para hacer una predicción en un nuevo dato, se toma una "votación por mayoría" entre los clasificadores. La clase con más votos es la elegida. Aunque también puede haber áreas de ambigüedad, estas son más pequeñas que en el método Uno-contra-Todo.

### Resumen

- **Regresión SoftMax**: Transforma regresión logística para clasificación multiclase usando una función de probabilidad. No es compatible con SVM.
- **Uno-contra-Todo**: Divide el problema en múltiples clasificadores binarios (uno para cada clase vs. todas las demás). Puede generar áreas ambiguas.
- **Uno-contra-Uno**: Divide el problema en clasificadores para cada par de clases, reduciendo las áreas de ambigüedad con votación por mayoría.

---

## Introducción a Clustering y sus Aplicaciones

### 1. ¿Qué es el Clustering?
El **clustering** es un enfoque no supervisado utilizado para agrupar datos en función de su similitud. Un ejemplo de aplicación es la **segmentación de clientes**:
- **Segmentación de clientes**: La práctica de dividir una base de clientes en grupos de individuos con características similares, lo que permite a las empresas asignar recursos de marketing de manera más eficiente.
    - Ejemplo de grupos: 
        - Clientes de alto beneficio y bajo riesgo.
        - Clientes de organizaciones sin fines de lucro.
- **Proceso general**: El clustering permite **segmentar grandes volúmenes de datos** con características como edad, género, intereses, hábitos de compra, etc., para identificar cómo los clientes son similares entre sí.

### 2. ¿Cómo Funciona el Clustering?
El **clustering** agrupa datos en función de la similitud de los puntos, sin supervisión, dividiendo el conjunto de datos en **grupos mutuamente excluyentes**.
- Ejemplo: Un conjunto de clientes puede ser segmentado en 3 **clusters**:
    1. Clientes acomodados de mediana edad.
    2. Jóvenes, educados y de ingresos medios.
    3. Jóvenes y de bajos ingresos.
- **Aplicación**: Cruzando este conjunto segmentado con datos sobre productos/servicios comprados, se puede entender y predecir las preferencias de compra y comportamientos de los clientes.

### 3. Clustering vs. Clasificación
La **clasificación** asigna etiquetas a los datos, es un enfoque supervisado, mientras que el **clustering** agrupa los datos sin etiquetas predefinidas.
- **Clasificación**: Se usa para predecir etiquetas categóricas (ej. cliente que va a incurrir en impago).
- **Clustering**: Es un enfoque no supervisado, donde los datos no tienen etiquetas y el algoritmo agrupa instancias similares, por ejemplo, a través de algoritmos como **K-Means**.

### 4. Aplicaciones del Clustering
El clustering tiene muchas aplicaciones en diferentes sectores:
- **Retail**: Para encontrar asociaciones entre clientes según sus características demográficas y patrones de compra.
- **Sistemas de recomendación**: Para identificar grupos de usuarios similares y realizar filtrado colaborativo, recomendando productos como libros o películas.
- **Banca**: Para detectar patrones de uso fraudulento de tarjetas de crédito y clasificar clientes (ej. leales vs. clientes perdidos).
- **Seguros**: Para detectar fraudes en reclamaciones o evaluar el riesgo de seguros de clientes según sus segmentos.
- **Medios de publicación**: Para categorizar automáticamente noticias y recomendar artículos similares a los lectores.
- **Medicina**: Para caracterizar el comportamiento de pacientes según características similares y encontrar terapias exitosas.
- **Biología**: Para agrupar genes con patrones de expresión similares o identificar relaciones familiares a través de marcadores genéticos.

### 5. Usos del Clustering
Generalmente, el clustering se puede usar para:
- **Análisis exploratorio de datos**.
- **Generación de resúmenes** o reducción de escala.
- **Detección de anomalías**, especialmente para fraude o eliminación de ruido.
- **Identificación de duplicados** en conjuntos de datos.
- Como un paso previo en tareas de **predicción**, **minería de datos** o **sistemas complejos**.

### 6. Tipos de Algoritmos de Clustering

#### 6.1. Clustering Basado en Particiones
- Produce clusters de forma esférica.
- Ejemplos: **K-Means**, **K-Medians**, **Fuzzy c-Means**.
- Usados para bases de datos medianas y grandes.

#### 6.2. Clustering Jerárquico
- Produce árboles de clusters.
- Ejemplos: Algoritmos **aglomerativos** y **divisivos**.
- Son intuitivos y buenos para bases de datos pequeñas.

#### 6.3. Clustering Basado en Densidad
- Produce clusters con formas arbitrarias.
- Especialmente útiles para manejar clusters espaciales o datos con ruido.
- Ejemplo: **DBSCAN**.

---
## K-Means Clustering

### 1. Introducción
- **K-Means Clustering** es un algoritmo de **clustering no supervisado**.
- Se utiliza para agrupar datos basándose en la similitud entre los puntos de datos.
- Un ejemplo común de uso es la **segmentación de clientes**, donde el objetivo es dividir a los clientes en grupos con características similares.

**Objetivo de K-Means:**
- Formar **K clusters** de manera que los puntos dentro de un mismo cluster sean lo más similares posible y los puntos de diferentes clusters lo más distintos posible.

### 2. ¿Cómo se mide la similitud?
- Se usan métricas de **distancia** para medir la similitud entre los puntos de datos.
- La **distancia Euclidiana** es la más comúnmente usada, especialmente en datos multidimensionales.

**Alternativas:**
- **Coseno de similitud**.
- **Distancia promedio**.

### 3. ¿Cómo funciona K-Means?

#### Pasos del algoritmo:

1. **Inicialización de centroides**:
   - Colocar aleatoriamente **K centroides** en el espacio de datos.

2. **Cálculo de distancias**:
   - Calcular la distancia de cada punto de datos a los centroides utilizando **distancia Euclidiana** (u otras métricas si se requiere).

3. **Asignación de puntos**:
   - Asignar cada punto al centroide más cercano, formando clusters.

4. **Recalcular los centroides**:
   - Después de asignar los puntos, recalcular la posición de los centroides como el promedio de todos los puntos dentro de cada cluster.

5. **Repetir el proceso**:
   - Continuar iterando hasta que los centroides ya no se desplacen.

#### Convergencia del algoritmo:
- El algoritmo es **iterativo** y continuará moviendo los centroides y reasignando puntos hasta que los centroides se estabilicen.
- El objetivo es **minimizar la distancia** entre los puntos de datos y sus centroides, pero puede llegar a un **óptimo local**.
- Para evitar óptimos locales, se recomienda ejecutar el algoritmo múltiples veces con diferentes inicializaciones.

### 4. Evaluación de la Calidad de los Clusters

#### ¿Cómo evaluar la bondad de los clusters?
1. **Comparación con la verdad de terreno** (si está disponible).
2. **Cálculo del error dentro del cluster**:
   - Medir la **distancia promedio** entre los puntos de datos y los centroides.

### 5. Determinación del Número de Clusters (K)

#### Método del Codo
- Para elegir el valor adecuado de **K**, se grafica la **distancia entre los puntos de datos y sus centroides** a medida que varía K.
- A medida que aumenta K, la distancia disminuye, pero llega un punto donde la disminución se desacelera. Este punto es conocido como **el punto de codo** y señala el número óptimo de clusters.

#### Métodos para encontrar el mejor K:
- Calcular la **distancia promedio** entre los puntos y los centroides, lo que indica qué tan densos son los clusters.
- Observar cómo cambia esta métrica al aumentar K, buscando el punto donde la tasa de disminución cambia abruptamente.

### 6. Resumen de K-Means

- **K-Means** es un algoritmo **basado en particiones** que es **eficiente** en conjuntos de datos medianos y grandes.
- Los clusters suelen tener una **forma esférica** debido a la distribución alrededor de los centroides.
- **Desventaja**: Se debe predefinir el número de clusters (**K**), lo que puede ser complicado si no se tiene conocimiento previo de los datos.

**Aplicaciones comunes de K-Means:**
- Segmentación de clientes.
- Análisis de patrones de compra.
- Identificación de fraudes.
- Sistemas de recomendación.

