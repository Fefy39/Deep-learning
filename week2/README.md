# Estudiante: Jenifer Cardenas Aguilera
# Deep Learning – Semana 1  
## Ejercicio práctico: Entiende una neurona en 15 minutos (Red 'vainilla')

Observar como cambia la salida de una neurona cuando modificas entradas, pesos (w1, w2) y el
sesgo (bias)

### Fórmula
- \( z = x_1 w_1 + x_2 w_2 + b \)


### Casos
- (0,0), (0,1), (1,0), (1,1)

### Bias probados
- **b = -0.5**
- **b = -1.0**
- **b = -2.0**

---

## Resultados

### b = -0.5
```
Entrada=(0,0) z=-0.5 salida=0
Entrada=(0,1) z=0.5 salida=1
Entrada=(1,0) z=0.5 salida=1
Entrada=(1,1) z=1.5 salida=1
```

### b = -1.0
```
Entrada=(0,0) z=-1.0 salida=0
Entrada=(0,1) z=0.0 salida=1
Entrada=(1,0) z=0.0 salida=1
Entrada=(1,1) z=1.0 salida=1
```

### b = -2.0
```
Entrada=(0,0) z=-2.0 salida=0
Entrada=(0,1) z=-1.0 salida=0
Entrada=(1,0) z=-1.0 salida=0
Entrada=(1,1) z=0.0 salida=1
```

---

## Respuestas

**1) ¿Con qué valor de b la neurona se comporta más parecido a AND?**  
Con **b = -2.0**, porque **solo** produce salida **1** cuando la entrada es **(1,1)** (igual que la compuerta AND).

**2) ¿Qué efecto tiene bajar o subir el bias en la salida? (1–2 líneas)**  
Si **b** se hace más negativo, **z** baja y es más difícil que \( z \ge 0 \) → salen menos **1**.  
Si **b** sube (menos negativo / más positivo), **z** sube y es más fácil que \( z \ge 0 \) → salen más **1**.
