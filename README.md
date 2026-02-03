# Clasificación de Audio Ambiental con Machine Learning 🎧

Este proyecto forma parte de la Maestría en Ciencias de la Computación y
consiste en desarrollar un sistema capaz de identificar entornos domésticos
a partir de grabaciones de audio cortas.

Se trabajó con un conjunto de datos colectivo de 198 muestras para
entrenamiento y 18 muestras para prueba, grabadas por diferentes personas
en distintos ambientes.

## 🧠 Descripción

El objetivo principal es transformar señales de audio crudas en descriptores
matemáticos y entrenar modelos de clasificación para distinguir entre
ambientes como *baño*, *cocina*, *sala* y otros.

Durante el desarrollo se realizaron los siguientes pasos principales:

- Carga y preprocesamiento de los archivos de audio.
- Extracción de características acústicas (MFCC).
- Manejo de valores faltantes y escalado de las características.
- Entrenamiento de varios modelos de aprendizaje automático.
- Evaluación con datos de prueba y análisis comparativo.

## 🛠️ Modelos utilizados

Se evaluaron distintos modelos, de los cuales se seleccionaron tres por su
robustez en conjuntos de datos pequeños y ruido presente en los audios:

- **Random Forest**: modelo basado en ensambles de árboles.
- **Extra Trees**: variante de Random Forest con mayor aleatoriedad.
- **KNN (K-Nearest Neighbors)**: modelo basado en vecinos más cercanos.

Extra Trees mostró un desempeño más equilibrado al analizar métricas
como el F1-score macro, aunque Random Forest presentó un accuracy global
ligeramente mayor. Esto indica que Extra Trees comete menos errores entre
clases similares y ofrece mayor consistencia general.

## 📊 Resultado general

Los modelos fueron evaluados con el conjunto de prueba proporcionado por
el profesor. Las métricas obtenidas y las matrices de confusión permiten
identificar qué clases fueron clasificadas correctamente y cuáles presentaron
mayor confusión.

Al revisar los audios de prueba manualmente se observó que varias muestras
etiquetadas como *baño* contenían sonidos de pasos u otros ruidos ambientales
que dificultan su clasificación automática, lo cual explica parte de los
errores observados.

## 📁 Requisitos

Para correr el notebook correctamente es necesario tener instalado:

- Python 3.x
- Librerías:
  - `librosa`
  - `scikit-learn`
  - `numpy`
  - `matplotlib`

Puedes instalarlas con:

```bash
pip install librosa scikit-learn numpy matplotlib

