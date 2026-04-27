# CADI Deep Learning - Semana 8
# # Semana 8: Implementación de un Modelo Popular de CNN en TensorFlow + Keras y/o PyTorch
# **Estudiante:** Jenifer Cárdenas Aguilera


## Dataset Usado
Se ha utilizado el dataset **CIFAR-10**, que consiste en 60,000 imágenes de 32x32 píxeles a color en 10 clases, con 6,000 imágenes por clase. Para este experimento, se han utilizado 5,000 imágenes para entrenamiento y 1,000 imágenes para pruebas.

## Arquitectura de Modelos
Se han empleado dos arquitecturas de red neuronal para la clasificación:
1.  **CNN Base Simplificada**: Una red convolucional con una capa `Conv2D`, una capa `MaxPooling2D`, `Flatten` y una capa `Dense` final.
2.  **Transfer Learning (MobileNetV2)**: Se utilizó el modelo pre-entrenado MobileNetV2 (`imagenet` weights) como extractor de características, con sus capas base congeladas (`trainable = False`), seguido de una capa `GlobalAveragePooling2D` y una capa `Dense` para la clasificación.

## Comparación Realizada
Se comparó el rendimiento de una **CNN base simplificada** (entrenada desde cero) con un enfoque de **Transfer Learning utilizando MobileNetV2** (congelado) para la tarea de clasificación de imágenes en el dataset CIFAR-10. Ambos modelos fueron entrenados con un número limitado de épocas para observar su comportamiento inicial.

## Resultado Principal
La **CNN Base Simplificada** obtuvo una precisión del **44.10%** en el conjunto de datos de prueba después de 3 épocas de entrenamiento.

El modelo de **Transfer Learning con MobileNetV2** fue entrenado, pero su evaluación final no fue mostrada en el notebook actual.

## Cómo Ejecutar
Para ejecutar este análisis, simplemente abra el notebook en Google Colab y ejecute todas las celdas de forma secuencial (`Runtime -> Run all`).

## Conclusiones
1.  La **CNN Base Simplificada** alcanzó una precisión inicial del 44.10% en el dataset CIFAR-10 con solo 3 épocas y un número reducido de datos de entrenamiento (5,000 imágenes).
2.  El modelo de **Transfer Learning con MobileNetV2** fue inicializado y entrenado por 2 épocas, pero su métrica de evaluación final no se calculó ni se mostró, lo que impide una comparación directa con la CNN base.
3.  Los resultados del modelo base sugieren que, con más épocas de entrenamiento y un dataset más grande, la precisión podría mejorar significativamente.
4.  La advertencia sobre `input_shape` en MobileNetV2 indica que la configuración de entrada de 32x32x3 no es la ideal para el modelo pre-entrenado, lo que podría afectar su rendimiento y la capacidad de aprovechar los pesos pre-entrenados de manera óptima para este tamaño de imagen.