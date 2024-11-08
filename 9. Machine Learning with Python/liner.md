# Regresión Lineal

Existen dos tipos básicos de modelos de regresión lineal:
- **Regresión Lineal Simple**: Aquí se utiliza una sola variable independiente para predecir una variable dependiente. Por ejemplo, si quisiéramos estimar las emisiones de CO₂ de un automóvil, podríamos usar como único factor el tamaño del motor.
- **Regresión Lineal Múltiple**: Este tipo de regresión incluye varias variables independientes para mejorar la precisión de las predicciones. Por ejemplo, para predecir las emisiones de CO₂ de un automóvil, además del tamaño del motor, también se pueden considerar el número de cilindros y el consumo de combustible.

## ¿Para Qué Sirve la Regresión Lineal Múltiple?
Este modelo es útil para dos tipos de aplicaciones:
1. **Evaluar el impacto de las variables independientes en la variable dependiente**: Por ejemplo, podemos analizar cómo variables como el tiempo de estudio, la asistencia a clases y el género afectan el rendimiento de un estudiante en un examen.
2. **Predecir cambios en la variable dependiente**: Nos permite prever cómo cambiará la variable dependiente si modificamos alguna de las variables independientes. Por ejemplo, podríamos estimar cuánto aumentará la presión arterial de una persona al incrementar su índice de masa corporal, manteniendo constantes otros factores.

## La Ecuación de Regresión Lineal Múltiple
En un modelo de regresión lineal múltiple, la variable objetivo **Y** se representa como una combinación lineal de las variables independientes (o predictoras), a las que llamaremos **X₁, X₂, X₃**, y así sucesivamente. La ecuación tiene la forma:

\[
\hat{y} = \theta_0 + \theta_1 X_1 + \theta_2 X_2 + \dots + \theta_n X_n
\]

Donde:
- **𝜃₀** es el intercepto (o constante de ajuste),
- **𝜃₁, 𝜃₂, \dots, 𝜃ₙ** son los coeficientes que muestran el peso o la importancia de cada variable en la predicción de **Y**.

En pocas palabras, la ecuación busca estimar los valores de estos coeficientes (**𝜃**) para que el modelo ajuste lo mejor posible los datos y minimice el error en las predicciones.

## Cómo Encontrar los Mejores Coeficientes (Optimización de Parámetros)
La optimización de los coeficientes **𝜃** se realiza buscando minimizar el error de las predicciones. Hay dos métodos comunes:
- **Mínimos Cuadrados Ordinarios (OLS)**: Es una técnica que minimiza el error cuadrático medio, útil cuando el tamaño del conjunto de datos es manejable (menos de 10,000 filas).
- **Algoritmos de Optimización**: Como el descenso por gradiente, que es eficaz para grandes conjuntos de datos. Este método comienza con valores aleatorios para los coeficientes y los ajusta iterativamente para reducir el error.

## Evaluación del Modelo: ¿Qué Tan Bien Predice?
Para evaluar el modelo, se calcula el error promedio de las predicciones con el **Error Cuadrático Medio (MSE)**. Un menor valor de MSE indica que el modelo está ajustando mejor los datos.

## Predicción con el Modelo
Una vez optimizados los coeficientes, la predicción es directa: solo se sustituyen los valores de las variables independientes en la ecuación para obtener el valor estimado de la variable objetivo.

Por ejemplo, si en el caso de emisiones de CO₂ encontramos que:

\[
Emisiones\ de\ CO₂ = 125 + (6.2 \times Tamaño\ del\ Motor) + (14 \times Número\ de\ Cilindros)
\]

Podríamos calcular el valor de emisiones para un automóvil específico insertando sus datos de tamaño de motor y cilindros en esta ecuación.

## Consideraciones Adicionales
- **Número de Variables**: Incluir muchas variables sin justificación teórica puede generar un modelo sobreajustado (overfitting), que no generaliza bien para otros datos. Se recomienda seleccionar solo
