# CADI Deep Learning - Semana 7
# # Semana 7: Implementación de la Convolución de Matrices y su Aplicación en Imágenes con Padding y Stride
# **Estudiante:** Jenifer Cárdenas Aguilera



### Objetivo
Comprender de forma práctica cómo la operación de convolución transforma una matriz de entrada y cómo el uso de Padding y Stride afecta las dimensiones finales del mapa de características.

### Comparación Realizada
Se utilizó una matriz base de 5x5 y un kernel de detección de bordes de 3x3 para comparar:
1. **Convolución Simple**: Sin relleno y con salto de 1 (Resultado: 3x3).
2. **Padding**: Relleno de 1 capa de ceros (Resultado: 5x5, preserva tamaño original).
3. **Stride**: Salto de 2 píxeles (Resultado: 2x2, reduce la dimensionalidad).

### Evidencia Principal
- La aplicación de **Padding=1** permitió recuperar la dimensión original de la imagen (5x5).
- El uso de **Stride=2** redujo el mapa de características a una cuarta parte de su tamaño original.

### Conclusiones Técnicas

1. **Preservación de Dimensiones:** El uso de `padding=1` permitió que la salida conservara el tamaño original de (5x5), demostrando que es vital para mantener la resolución espacial en capas profundas.
2. **Compresión de Información:** El `stride=2` redujo la matriz de (5x5) a (2x2). Esto evidencia que un paso mayor actúa como un método de submuestreo (downsampling) efectivo para reducir carga computacional.
3. **Efecto de Borde:** Sin padding, los píxeles de las esquinas solo se procesan una vez, lo que genera una pérdida de información periférica reflejada en la reducción de (5x5) a (3x3).

### Cómo ejecutar
1. Abrir `Week.ipynb` en Google Colab.
2. Ejecutar todas las celdas para visualizar las matrices resultantes y las gráficas de calor.