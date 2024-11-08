# 11. Generative AI: Elevate Your Data Science Career

Trabajos del curso la IA generativa en el ámbito de la ciencia de datos. A través de esta tecnología, podrás generar contenido diverso (imágenes, texto, código, música) y enfrentar problemas comunes como la escasez de datos, el sesgo en datos, y la necesidad de crear datos realistas para entrenamiento de modelos.

Este curso está dirigido a científicos de datos, analistas y profesionales de datos interesados en explorar el potencial de la IA generativa para mejorar y acelerar los flujos de trabajo en ciencia de datos, garantizando un uso ético e innovador.

## Estructura del Curso

Este es el tercer curso del programa de IA Generativa para Ciencia de Datos y está dividido en tres módulos:

### Módulo 1: Introducción a Herramientas y Aplicaciones
- Introducción a las herramientas de IA generativa para ciencia de datos.
- Aplicaciones de la IA generativa en diversas industrias, incluyendo la preparación de datos y consulta de bases de datos.

### Módulo 2: Análisis y Visualización de Datos con IA Generativa
- Uso de IA generativa para extraer información y visualizar datos.
- Desarrollo de modelos de predicción eficientes con IA generativa y revisión de los desafíos éticos y técnicos en ciencia de datos.

### Módulo 3: Proyecto Final y Evaluación
- Realización de un proyecto final aplicando todo lo aprendido.
- Repaso de conceptos clave y evaluación final del curso.


## Guía para elegir un tipo de modelo de IA Generativa

### Tipos de modelos de IA generativa

| Modelo                         | Características clave                                                                                             | Aplicaciones                                                                                   |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| **Redes Generativas Antagónicas (GANs)** | Dos redes neuronales en competencia: generador y discriminador. El generador aprende a crear datos realistas, mientras que el discriminador aprende a distinguir entre datos reales y falsos. El proceso de entrenamiento adversarial mejora continuamente ambas redes. Puede ser difícil de entrenar y obtener resultados estables. | Generación de imágenes: caras, paisajes, objetos. Generación de texto: poemas, código, guiones. Generación de video: videos realistas, animación. Descubrimiento de fármacos: generar moléculas con propiedades deseadas. Generación de música: composición de nuevas canciones. |
| **Autoencoders Variacionales (VAEs)** | Codifica los datos de entrada en un espacio latente de menor dimensión. Aprende una distribución de probabilidad sobre el espacio latente. Decodifica muestras del espacio latente para generar nuevos puntos de datos. Se enfoca en aprender una representación significativa de los datos. | Compresión de imágenes: almacenamiento y transmisión eficiente de imágenes. Detección de anomalías: identificar puntos de datos inusuales. Reducción de dimensionalidad: comprimir datos de alta dimensión. Resumen de textos: generar resúmenes concisos de documentos de texto. |
| **Modelos Autoregresivos**      | Genera datos punto por punto, condicionados a los puntos generados previamente. Usa redes neuronales recurrentes (RNN) o transformadores para capturar dependencias a largo plazo. Puede ser costoso computacionalmente para secuencias largas. | Generación de texto: secuencias de texto realistas y coherentes. Generación de música: generar música que sigue el género y estilo. Pronóstico de series temporales: predecir valores futuros de una serie temporal. Pintura de imágenes: rellenar partes faltantes de una imagen. |
| **Modelos de Difusión**         | Comienza con un ruido simple y gradualmente lo "desrueda" para convertirlo en datos realistas. Utiliza una arquitectura U-Net con conexiones de salto para preservar la información. Puede ser más estable y fácil de entrenar que los GANs, pero generalmente más lento. | Generación de imágenes: imágenes de alta calidad y diversas. Generación de texto: texto coherente y gramaticalmente correcto. Generación de audio: audio realista y musical. Pintura y eliminación de ruido: mejorar la calidad de imágenes o audio. |
| **Modelos Basados en Flujos**   | Transforma una distribución simple (Gaussiana) en una compleja usando transformaciones invertibles. Aprende los parámetros de estas transformaciones a partir de los datos. Puede ser eficiente y preciso para datos de alta dimensión, pero el entrenamiento puede ser desafiante. | Generación de imágenes: imágenes realistas y diversas. Estimación de densidad: modelado de la distribución de probabilidad de los datos. Reducción de dimensionalidad: comprimir datos de alta dimensión. Detección de anomalías: identificar puntos de datos inusuales. |

### Comparación de modelos según diferentes consideraciones

| Característica                  | GANs                   | VAEs                   | Modelos Autoregresivos    | Modelos de Difusión       | Modelos Basados en Flujos |
|----------------------------------|------------------------|------------------------|---------------------------|---------------------------|---------------------------|
| Tipo de datos                    | Imágenes, texto, audio | Imágenes, texto, datos continuos | Imágenes, texto, secuencias | Imágenes, texto           | Imágenes, datos continuos |
| Objetivo de la tarea             | Generación de alta fidelidad, aumento de datos | Codificación/decodificación, aprendizaje de representaciones | Generación de secuencias, traducción de texto a imagen | Generación de imágenes, edición, pintura | Generación de imágenes, generación condicional |
| Calidad de las muestras          | Alta fidelidad, diversas | A menudo borrosas, menos realistas | Nítidas, alta resolución | Alta fidelidad, diversas  | Alta fidelidad, controlable |
| Control sobre la generación     | Limitado               | Moderado               | Alto                      | Moderado                  | Alto                      |
| Complejidad de entrenamiento    | Alta                   | Moderada               | Alta                      | Moderada                  | Alta                      |
| Interpretabilidad                | Baja                   | Moderada               | Alta                      | Moderada                  | Baja                      |

