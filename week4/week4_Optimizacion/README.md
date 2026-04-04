# Programa: Esp. Inteligencia Artificial
# Materia: Deep learning
# Alumno: Jenifer Cardenas Aguilera. 
# Week 4 - Aplicación de Técnicas de optmimización en una Red Neuronal 

## Objetivo
Comparar el efecto de dos técnicas de optimización, **SGD** y **Adam**, en el entrenamiento de una red neuronal, con el fin de analizar su impacto sobre la convergencia, el error y la capacidad de generalización del modelo.

## Técnica(s) comparada(s)
En esta actividad se compararon dos configuraciones de entrenamiento:
- **SGD (lr=0.01)**
- **Adam (lr=0.001)**

## Configuración base
Se utilizó el mismo dataset, la misma arquitectura de red neuronal, la misma división entre entrenamiento y prueba y los mismos hiperparámetros generales.  
La única diferencia entre las configuraciones fue el **optimizador**.

## Comparación realizada
Se entrenó una red neuronal con dos optimizadores distintos, manteniendo constantes los demás elementos, para observar diferencias en `loss`, `accuracy`, estabilidad del entrenamiento y desempeño final.

## Resultado principal
El mejor resultado lo obtuvo **Adam (lr=0.001)**, con un **test accuracy de 0.973684** y un **test loss de 0.074451**, superando a **SGD (lr=0.01)**, que alcanzó un **test accuracy de 0.921053** y un **test loss de 0.199449**.  
Esto evidencia una convergencia más eficiente y una mejor generalización con Adam.

## Cómo ejecutar el notebook
1. Abrir el archivo `.ipynb` en **Google Colab**.
2. Ejecutar todas las celdas en orden, desde la primera hasta la última.
3. Verificar las tablas, gráficas y métricas finales generadas por el notebook.
