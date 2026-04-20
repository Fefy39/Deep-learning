# Programa: Esp. Inteligencia Artificial
# Materia: Deep learning
# Alumno: Jenifer Cardenas Aguilera.
# CADI Deep Learning - Semana 5
## Técnicas de Optimización e Hiperparámetros

### 1. Objetivo
Evidenciar cómo el desempeño y la estabilidad del entrenamiento de una red neuronal cambian al ajustar la tasa de aprendizaje (**Learning Rate**) utilizando el dataset MNIST.

### 2. Comparación de Hiperparámetros
En este ejercicio se configuraron dos variables para validar cómo varía el aprendizaje del modelo, manteniendo la arquitectura constante:

* **Modelo A (LRATE - 0.0001):** Learning Rate bajo. Los pasos son pequeños, el modelo aprende lento y los cambios en los pesos son mínimos. Es un entrenamiento estable y menos propenso a desestabilizarse, aunque puede tardar mucho en converger.
* **Modelo B (HRATE - 0.01):** Learning Rate alto. Los pasos son más grandes y el aprendizaje es mucho más rápido. El modelo tarda menos tiempo en entrenar y converge rápido.

### 3. Evidencia Principal (Conclusiones)
A partir de la ejecución y las gráficas obtenidas, se concluye:
* **Estabilidad:** El modelo con LR bajo (0.0001) genera curvas de entrenamiento suavizadas, confirmando su estabilidad frente al ruido.
* **Convergencia:** El modelo con LR alto (0.01) alcanza resultados óptimos en menos épocas, pero presenta "rebotes" o inestabilidad en la pérdida de validación debido a la magnitud de sus pasos.
* **Hallazgo:** La elección del LR depende del tiempo disponible; mientras el LR alto es eficiente en velocidad, el LR bajo es superior para lograr un ajuste fino y preciso de los pesos.

### 4. Cómo ejecutar
1. Abrir el archivo `week5/Week5.ipynb` en Google Colab.
2. Ejecutar todas las celdas para observar la comparativa entre **LRATE** y **HRATE**.