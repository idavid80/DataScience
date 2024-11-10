# Guía Rápida

## Herramientas de IA Generativa para Científicos de Datos

| **Tarea**                           | **Descripción**                                                                                             | **Herramientas**                                         | **Propósito y Aplicaciones**                                                                                                                                          |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Generación de datos sintéticos**  | Creación de muestras de datos artificiales que imitan conjuntos de datos reales.                            | TensorFlow Probability, PyTorch, SDV, GANs               | TensorFlow Probability y PyTorch permiten el modelado probabilístico, mientras que SDV genera datos sintéticos basados en modelos estadísticos. GANs crean muestras de datos realistas. Estas herramientas se usan en sanidad para registros de pacientes sintéticos, en finanzas para transacciones simuladas, y para entrenar modelos de aprendizaje automático con datos escasos o sensibles. |
| **Generación y manipulación de imágenes** | Generación de imágenes sintéticas, modificación de atributos visuales, y creación de nuevos diseños.    | StyleGAN, DALL-E, BigGAN                                | StyleGAN genera imágenes de alta calidad, DALL-E crea imágenes a partir de descripciones de texto, y BigGAN genera imágenes diversas y realistas. Estas herramientas tienen aplicaciones en arte y diseño, creación de contenido, moda y videojuegos, facilitando la creación de imágenes únicas y flujos creativos. |
| **Generación de lenguaje natural**  | Generación de texto similar al humano, creación de historias, artículos o diálogos.                        | Modelos GPT de OpenAI, Transformadores de Hugging Face   | Los modelos GPT generan texto coherente y adecuado al contexto, mientras que los transformadores permiten flexibilidad en la generación de texto y ajuste a tareas específicas. Estas herramientas se utilizan en chatbots, generación de contenido, resumen automático y IA conversacional en medios, servicio al cliente y creación de contenido. |
| **Síntesis de música y audio**      | Generación de composiciones musicales o muestras de audio sintetizadas.                                     | Magenta, Jukebox, NSynth                                 | Magenta genera melodías y composiciones usando técnicas de aprendizaje profundo, Jukebox crea canciones en varios géneros, y NSynth genera nuevos sonidos combinando los existentes. Artistas usan estas herramientas en producción musical, videojuegos y entretenimiento para crear composiciones originales, efectos de sonido y bandas sonoras adaptativas. |
| **Simulación y aumento de datos**   | Simulación de escenarios y aumento de conjuntos de datos para modelos de aprendizaje automático.           | Unity ML-Agents, SimNet de NVIDIA, Augmentor             | Unity ML-Agents crea agentes inteligentes para simulaciones, SimNet simula datos realistas, y Augmentor proporciona técnicas de aumento de datos. Profesionales de datos usan estas herramientas en robótica, videojuegos, vehículos autónomos y simulaciones para entrenar modelos de IA y probar algoritmos en diferentes entornos. |
| **Generación de contenido**         | Creación de contenido similar al humano, como texto, imágenes y música.                                    | Modelos GPT de OpenAI, DeepDream, StyleGAN               | Los modelos GPT destacan en la generación de texto coherente, DeepDream crea imágenes surrealistas, y StyleGAN asegura la generación de imágenes realistas. Creadores de contenido utilizan estas herramientas en creación de contenido, narrativa, arte e industrias de entretenimiento. |
| **Detección de anomalías**          | Identificación de valores atípicos o anomalías en conjuntos de datos.                                      | Autoencoders, Isolation Forest, GANs                     | Los autoencoders detectan anomalías en los datos, Isolation Forest maneja eficazmente la detección de anomalías en datos de alta dimensión, y GANs generan distribuciones normales de datos. Se usan para detectar fraudes financieros, errores de manufactura y en ciberseguridad. |
| **Aumento de datos**                | Mejora de conjuntos de datos de entrenamiento generando variaciones de datos existentes.                    | CycleGAN, Augmentor, Transferencia de Estilo Neuronal    | CycleGAN realiza traducción de imagen a imagen, Augmentor genera imágenes aumentadas, y la Transferencia de Estilo Neuronal transforma artísticamente imágenes en función del estilo de una imagen y el contenido de otra. Se usan en visión por computadora, imágenes médicas y para aumento de datos en modelos de aprendizaje automático. |
| **Interacción humano-computadora**  | Permitir interacciones similares a las humanas a través de chatbots, asistentes y avatares.                | Dialogflow, Rasa, RunwayML                               | Dialogflow y Rasa construyen eficazmente IA conversacional, mientras que RunwayML es adecuado para la codificación creativa. Estas herramientas se utilizan en servicio al cliente, asistentes virtuales e industrias de videojuegos para mejorar la experiencia del usuario. |

---

## Guía para elegir un tipo de modelo de IA Generativa

### Tipos de modelos de IA generativa

| Modelo                         | Características clave                                                                                             | Aplicaciones                                                                                   |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| **Redes Generativas Antagónicas (GANs)** | Dos redes neuronales en competencia: generador y discriminador. El generador aprende a crear datos realistas, mientras que el discriminador aprende a distinguir entre datos reales y falsos. El proceso de entrenamiento adversarial mejora continuamente ambas redes. Puede ser difícil de entrenar y obtener resultados estables. | Generación de imágenes: caras, paisajes, objetos. Generación de texto: poemas, código, guiones. Generación de video: videos realistas, animación. Descubrimiento de fármacos: generar moléculas con propiedades deseadas. Generación de música: composición de nuevas canciones. |
| **Autoencoders Variacionales (VAEs)** | Codifica los datos de entrada en un espacio latente de menor dimensión. Aprende una distribución de probabilidad sobre el espacio latente. Decodifica muestras del espacio latente para generar nuevos puntos de datos. Se enfoca en aprender una representación significativa de los datos. | Compresión de imágenes: almacenamiento y transmisión eficiente de imágenes. Detección de anomalías: identificar puntos de datos inusuales. Reducción de dimensionalidad: comprimir datos de alta dimensión. Resumen de textos: generar resúmenes concisos de documentos de texto. |
| **Modelos Autoregresivos**      | Genera datos punto por punto, condicionados a los puntos generados previamente. Usa redes neuronales recurrentes (RNN) o transformadores para capturar dependencias a largo plazo. Puede ser costoso computacionalmente para secuencias largas. | Generación de texto: secuencias de texto realistas y coherentes. Generación de música: generar música que sigue el género y estilo. Pronóstico de series temporales: predecir valores futuros de una serie temporal. Pintura de imágenes: rellenar partes faltantes de una imagen. |
| **Modelos de Difusión**         | Comienza con un ruido simple y gradualmente lo "desrueda" para convertirlo en datos realistas. Utiliza una arquitectura U-Net con conexiones de salto para preservar la información. Puede ser más estable y fácil de entrenar que los GANs, pero generalmente más lento. | Generación de imágenes: imágenes de alta calidad y diversas. Generación de texto: texto coherente y gramaticalmente correcto. Generación de audio: audio realista y musical. Pintura y eliminación de ruido: mejorar la calidad de imágenes o audio. |
| **Modelos Basados en Flujos**   | Transforma una distribución simple (Gaussiana) en una compleja usando transformaciones invertibles. Aprende los parámetros de estas transformaciones a partir de los datos. Puede ser eficiente y preciso para datos de alta dimensión, pero el entrenamiento puede ser desafiante. | Generación de imágenes: imágenes realistas y diversas. Estimación de densidad: modelado de la distribución de probabilidad de los datos. Reducción de dimensionalidad: comprimir datos de alta dimensión. Detección de anomalías: identificar puntos de datos inusuales. |

## Comparación de modelos según diferentes consideraciones

| Característica                  | GANs                   | VAEs                   | Modelos Autoregresivos    | Modelos de Difusión       | Modelos Basados en Flujos |
|----------------------------------|------------------------|------------------------|---------------------------|---------------------------|---------------------------|
| Tipo de datos                    | Imágenes, texto, audio | Imágenes, texto, datos continuos | Imágenes, texto, secuencias | Imágenes, texto           | Imágenes, datos continuos |
| Objetivo de la tarea             | Generación de alta fidelidad, aumento de datos | Codificación/decodificación, aprendizaje de representaciones | Generación de secuencias, traducción de texto a imagen | Generación de imágenes, edición, pintura | Generación de imágenes, generación condicional |
| Calidad de las muestras          | Alta fidelidad, diversas | A menudo borrosas, menos realistas | Nítidas, alta resolución | Alta fidelidad, diversas  | Alta fidelidad, controlable |
| Control sobre la generación     | Limitado               | Moderado               | Alto                      | Moderado                  | Alto                      |
| Complejidad de entrenamiento    | Alta                   | Moderada               | Alta                      | Moderada                  | Alta                      |
| Interpretabilidad                | Baja                   | Moderada               | Alta                      | Moderada                  | Baja                      |

## Hoja de Referencia del Tema 1: Introducción a Herramientas y Aplicaciones

### Herramientas Populares de GenAI

| Nombre del Modelo | Uso | Enlace |
|-------------------|-----|--------|
| Data Robot        | Herramienta simple útil para análisis de datos y operaciones de creación de modelos | [https://www.datarobot.com/](https://www.datarobot.com/) |
| Mostly.AI         | Generación de datos sintéticos | [https://mostly.ai/](https://mostly.ai/) |
| ChatGPT           | Modelo basado en GPT usado para generación de texto y código a partir de consultas en lenguaje natural | [https://openai.com/chatgpt](https://openai.com/chatgpt) |
| DB Sensei         | Genera consultas SQL para bases de datos usando consultas en lenguaje natural | [https://dbsensei.com/](https://dbsensei.com/) |

### Indicaciones Importantes para la Preparación de Datos

| Tarea | Prompt |
|-------|--------|
| Leer un archivo de datos CSV y cargarlo en un marco de datos | Escribe un código en Python que pueda realizar las siguientes tareas: <br> Leer el archivo CSV ubicado en una ruta de archivo específica en un marco de datos de Pandas, asumiendo que las primeras filas del archivo son los encabezados de los datos. |
| Limpieza de datos: Identificar y reemplazar valores faltantes según las siguientes pautas | Escribe un código en Python para realizar las siguientes tareas: <br> 1. Identificar los atributos con valores faltantes.<br> 2. Segregar estos atributos en categóricos y continuos.<br> 3. Eliminar la fila completa si el valor falta en la variable objetivo.<br> 4. Si el valor falta en un atributo categórico, reemplazar los valores faltantes con el valor más frecuente en la columna.<br> 5. Si el valor falta en un atributo de valor continuo, reemplazar los valores faltantes con el valor medio de los registros en la columna. |
| Normalización de datos: Normalizar un atributo a su valor máximo | Escribe un código en Python para normalizar el contenido de un atributo dado en un marco de datos `df` a su valor máximo. Realiza los cambios en los datos originales y no crees un nuevo atributo. |
| Convertir una variable categórica en variables indicadoras | Escribe un código en Python para realizar las siguientes tareas:<br> 1. Convertir un atributo de un marco de datos `df` en variables indicadoras, guardadas como `df1`, con la convención de nombres `"Nombre_<valor único del atributo>"`.<br> 2. Agregar `df1` al marco de datos original `df`.<br> 3. Eliminar el atributo original del marco de datos `df`. |



## IA Generativa Responsable para Profesionales de Datos

La IA generativa, incluyendo modelos como GPT-3 o GPT-4, presenta tanto desafíos como oportunidades. Los desafíos incluyen cuestiones de sesgo y equidad, uso ético, explicabilidad, preocupaciones de privacidad e impacto ambiental. 

| **Sección**                     | **Descripción**                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

| **IA Responsable**              | Trabajar los 5 pilares: Explicabilidad, Equidad, Robustez, Transparencia y Privacidad. Esto fomenta la transparencia, la rendición de cuentas y establece pautas éticas y estándares de la industria. Además, incluye técnicas de preservación de la privacidad como el aprendizaje federado o la privacidad diferencial.       |
| **Cumplimiento Legal y Normativo** | La IA responsable garantiza que los sistemas de IA cumplan con las leyes y regulaciones existentes, previniendo problemas relacionados con prácticas poco éticas. Estas prácticas también guían futuras regulaciones y estándares.                                                                                                                     |
| **Impacto Social**              | La IA responsable aborda preocupaciones éticas, sociales y prácticas, promoviendo el desarrollo de sistemas de IA que contribuyen positivamente a la sociedad. Fomenta el diseño inclusivo, evita la discriminación y promueve prácticas sostenibles en la IA. La viabilidad a largo plazo también es crucial para evitar rechazos públicos y restricciones. |
| **Prácticas de IA Responsable** | Incluye transparencia, inclusividad, monitorización continua, colaboración, empoderamiento del usuario, educación y cumplimiento legal. Es crucial ser transparente sobre las capacidades de los modelos de IA, asegurar una representación inclusiva y cumplir con regulaciones emergentes.                                                            |

                                                                                   |


## Hoja de Referencia del Tema 2: Análisis y Visualización de Datos con IA Generativa

### Herramientas Populares de IA Generativa

| Nombre del modelo | Uso                                                    | Enlace                        |
|-------------------|--------------------------------------------------------|-------------------------------|
| Hal9             | Herramienta de EDA para identificar conocimientos clave en los datos | [hal9.com](https://www.hal9.com/)        |
| Columns.ai       | Herramienta de visualización de datos para crear gráficos útiles     | [columns.ai](https://columns.ai/)        |
| Akkio            | Herramienta de visualización de datos para crear gráficos como gráficos de regresión, diagramas de caja, mapas de calor de correlación, entre otros | [akkio.com](https://www.akkio.com/) |

### Indicaciones importantes para generar conocimientos y visualizaciones de datos

| Tarea                                                               | Indicaciones                                                                                                                                                              |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Generar una descripción estadística de los datos.                   | Escribe un código en Python para generar la descripción estadística de todas las características utilizadas en el conjunto de datos. Incluye también los tipos de datos "object". |
| Crear gráficos de regresión entre una variable objetivo y una variable de origen continua. | Escribe un código en Python para generar un gráfico de regresión entre una variable objetivo y una variable de origen en un marco de datos.                               |
| Crear diagramas de caja entre una variable objetivo y una variable categórica de origen. | Escribe un código en Python para generar un diagrama de caja entre una variable objetivo y una variable de origen en un marco de datos.                                   |
| Evaluar la interdependencia paramétrica utilizando correlación, valor p y coeficiente de Pearson | Escribe un código en Python para evaluar la correlación, el coeficiente de Pearson y los valores p para todos los atributos de un marco de datos en relación con el atributo objetivo. |
| Agrupar variables para crear tablas dinámicas y realizar un gráfico de color p para la tabla dinámica. | Escribe un código en Python que realice las siguientes acciones: <br> 1. Agrupa tres atributos en un marco de datos (df). <br> 2. Crea una tabla dinámica para este grupo, usando un atributo objetivo y la función de agregación media. <br> 3. Realiza un gráfico de color p para esta tabla dinámica. |

### Indicaciones importantes para el desarrollo y refinamiento de modelos

| Tarea                                                                                       | Indicaciones                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Regresión lineal entre un solo atributo de origen y un atributo objetivo, y evaluación | Escribe un código en Python que realice las siguientes tareas: <br> 1. Desarrolla y entrena un modelo de regresión lineal que utilice un atributo de un marco de datos como variable de origen y otro como variable objetivo. <br> 2. Calcula y muestra los valores de MSE y R^2 para el modelo entrenado. |
| Regresión lineal entre múltiples atributos de origen y un atributo objetivo, y evaluación | Escribe un código en Python que realice las siguientes tareas: <br> 1. Desarrolla y entrena un modelo de regresión lineal que utilice algunos atributos de un marco de datos como variables de origen y un atributo como variable objetivo. <br> 2. Calcula y muestra los valores de MSE y R^2 para el modelo entrenado. |
| Modelo de regresión polinómica con un solo atributo de origen y uno objetivo               | Escribe un código en Python que realice las siguientes tareas: <br> 1. Desarrolla y entrena múltiples modelos de regresión polinómica, de órdenes 2, 3 y 5, que utilicen un atributo de un marco de datos como variable de origen y otro como variable objetivo. <br> 2. Calcula y muestra los valores de MSE y R^2 para los modelos entrenados. <br> 3. Compara el rendimiento de los modelos. |
| Creación de una tubería para escalado, creación de características polinómicas y regresión lineal | Escribe un código en Python que realice las siguientes tareas: <br> 1. Crea una tubería que realice el escalado de parámetros, la generación de características polinómicas y la regresión lineal. Usa el conjunto de múltiples características como antes para crear esta tubería. <br> 2. Calcula y muestra los valores de MSE y R^2 para el modelo entrenado. |
| Búsqueda en cuadrícula con regresión Ridge y validación cruzada                             | Escribe un código en Python que realice las siguientes tareas: <br> 1. Usa características polinómicas para algunos de los atributos de un marco de datos. <br> 2. Realiza una búsqueda en cuadrícula en un modelo de regresión Ridge para un conjunto de valores del hiperparámetro alfa y características polinómicas como entrada. <br> 3. Usa la validación cruzada en la búsqueda en cuadrícula. <br> 4. Evalúa los valores de MSE y R^2 del modelo resultante. |


## Puntos claves

- La IA generativa permite a los científicos de datos generar datos completamente nuevos, desbloqueando un universo de posibilidades y abordando desafíos previamente insuperables.

- Existen cuatro modelos estándar de IA generativa: Las redes generativas adversariales (GAN), los autocodificadores variacionales (VAE), los modelos autorregresivos y los modelos basados en flujos.  

- Mientras que las GAN son excelentes para el aumento de datos, los VAE son buenos para la detección de anomalías, la compresión de datos, el filtrado colaborativo y la transferencia de estilos. 

- Los modelos autorregresivos son buenos para la generación de textos, la síntesis de voz, la predicción de series temporales y la traducción automática, y los modelos basados en flujos son adecuados para la generación de imágenes y datos y la estimación de densidades.  

- La IA generativa puede abordar problemas complejos en diversos sectores. 

- Los modelos de IA generativa son fundamentales para afrontar varios retos de preparación y consulta de datos, como la introducción de valores perdidos, la detección de valores atípicos, la reducción del «ruido» y la traducción de consultas en lenguaje natural a sentencias SQL equivalentes.

- La IA generativa puede ayudar en el análisis exploratorio de datos o AED utilizando diversas técnicas, como la descripción estadística de datos, el análisis univariante, bivariante y multivariante, la ingeniería de características y la generación de hipótesis. 

- La IA generativa desempeña un papel importante en el desarrollo de un modelo predictivo utilizando diversas técnicas, como la selección de la arquitectura del modelo y las características esenciales, la generación de modelos de conjunto, la mejora de la interpretabilidad y la generalización del modelo, y la prevención del sobreajuste.

- Al utilizar modelos de IA generativa, los científicos de datos deben tener en cuenta los datos, los modelos y las consideraciones éticas.

- Los profesionales de los datos se enfrentan a diversos retos técnicos, organizativos y culturales cuando utilizan la IA generativa en múltiples sectores. 

- Ser un científico de datos de éxito requiere varias habilidades, como conocimientos matemáticos y estadísticos, conocimientos de lenguajes de programación y comprensión de los principios del aprendizaje automático.

## Preguntas frecuentes

**- ¿Consideraciones clave del modelo?**
**Explicabilidad**: La explicabilidad es una consideración fundamental en el desarrollo de modelos, ya que permite a los usuarios y a las partes interesadas entender cómo el modelo toma decisiones, lo que es esencial para la transparencia y la confianza.

**- ¿Técnica para comprobar la parcialidad en la aprobación de préstamos financieros?**
**Métricas de equidad**: Las métricas de imparcialidad ayudan a evaluar y cuantificar posibles sesgos dentro de un modelo, especialmente en áreas como la aprobación de préstamos, donde la imparcialidad es fundamental.

**- ¿Desafío técnico de la IA generativa?**
**Falta de estandarización**: En la IA generativa, a menudo hay una falta de estandarización entre herramientas, metodologías y mejores prácticas, lo que puede obstaculizar la implementación y la coherencia.

**- ¿Causa de las alucinaciones de la IA?**
**Datos de entrenamiento defectuosos**: Las alucinaciones de la IA suelen deberse a datos de entrenamiento defectuosos o insuficientes, que pueden llevar al modelo a generar resultados incorrectos o sin sentido.

**- ¿Consideración que se incumple al manipular la opinión pública con IA generativa?**
**Ética**: Manipular la opinión pública es una violación ética, ya que implica utilizar la IA de forma que pueda perjudicar a las personas o a las sociedades, en particular difundiendo información errónea o influyendo injustamente en las opiniones.