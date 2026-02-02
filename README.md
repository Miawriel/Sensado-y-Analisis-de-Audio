Clasificación de Audio Ambiental con ML 🎙️🤖
Este proyecto es parte de la Maestría en Ciencias de la Computación y consiste en el desarrollo de un sistema capaz de identificar 7 entornos domésticos diferentes a partir de grabaciones de audio cortas. Se utilizó un dataset colectivo de 180 muestras grabadas por distintas personas.

🚀 Resumen del Proyecto
El objetivo principal fue transformar señales de audio crudas en descriptores matemáticos (MFCCs) para entrenar y comparar la eficacia de tres modelos de clasificación: SVM (Lineal), Random Forest y una Red Neuronal (MLP).

🛠️ Pasos Clave del Preprocesamiento:
Limpieza de Etiquetas: Estandarización de nombres y unificación de categorías (minúsculas, eliminación de espacios y corrección de variaciones).

Eliminación de Ruidos Estacionarios: Uso de librosa.effects.trim para descartar silencios y ruidos de fondo en los extremos de las grabaciones.

Normalización: Ajuste de amplitud para compensar las diferencias de volumen entre los distintos dispositivos de grabación.

📊 Hallazgos Principales
Mejor Modelo: El Random Forest logró el desempeño más alto con un 64% de accuracy, seguido de cerca por el MLP con un 61%. Ambos demostraron ser superiores para manejar la variabilidad del dataset colectivo tras el preprocesamiento.

Clase Perfecta: La Sala fue identificada con un F1-score de 1.00 en todos los modelos, confirmando que posee una firma acústica sumamente distintiva.

Análisis del Baño vs Nula: Se identificó una confusión recurrente entre estas clases. Esto se atribuye a que la clase "Nula" (sonidos ambientales desconocidos) comparte frecuencias similares con el flujo de agua turbulento (WC) registrado en la categoría baño.

📋 Requisitos:

Python 3.x

Librosa

Scikit-learn

Pandas / Numpy
