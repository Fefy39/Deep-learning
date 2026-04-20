# CADI Deep Learning - Semana 6
# # Semana 6: Bias/Variance, Overfitting y Regularización
# **Estudiante:** Jenifer Cárdenas Aguilera



### 1. Objetivo
Analizar el comportamiento de una red neuronal frente al sobreajuste y aplicar métodos de regularización para mejorar la generalización del modelo.

### 2. Técnicas de Regularización Aplicadas
* **Regularización L2 (Penalización de pesos):** Para evitar que los pesos tomen valores excesivamente grandes.
* **Dropout (40%):** Para reducir la dependencia entre neuronas y forzar un aprendizaje robusto.
* **Early Stopping:** Para detener el entrenamiento en el punto óptimo antes de que ocurra overfitting.

### 3. Comparación Realizada
Se comparó un modelo de alta capacidad (256-128 neuronas) sin restricciones frente al mismo modelo utilizando las tres técnicas mencionadas, observando la evolución de la métrica `loss` en entrenamiento vs. validación.

### 4. Cómo ejecutar
1. Abrir el archivo `week6/Week6_Regularizacion.ipynb` en Google Colab.
2. Asegurarse de cargar las librerías `tensorflow`, `sklearn` y `matplotlib`.
3. Seleccionar `Entorno de ejecución` > `Ejecutar todo`.