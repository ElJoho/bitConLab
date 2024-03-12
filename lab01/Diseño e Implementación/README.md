La función de trasnferencia obtenida es:
$G_{(s)} = \frac{0.001147}{s^2 + 0.2808 s + 0.001112}$


Para diseñar controladores proporcional (P) y proporcional-integral (PI) para una función de transferencia dada, vamos a seguir un enfoque sistemático. La función de transferencia que nos das es:

$T(s) = \frac{0.001147}{s^2 + 0.2808s + 0.001112}$

### Controlador Proporcional (P)

El controlador proporcional se puede representar por la función de transferencia $C(s) = K_p$, donde $K_p$ es la ganancia proporcional.

La función de transferencia del sistema en lazo cerrado con solo un controlador proporcional sería:

$ T_{cl}(s) = \frac{K_p G(s)}{1 + K_p  G(s)} $

donde $G(s) = T(s)$ es la función de transferencia del sistema.

### Controlador Proporcional-Integral (PI)

El controlador PI se puede representar por la función de transferencia $C(s) = K_p + \frac{K_i}{s}$, donde $K_p$ es la ganancia proporcional y $K_i$ es la ganancia integral.

La función de transferencia del sistema en lazo cerrado con un controlador PI sería:

$ T_{cl}(s) = \frac{(K_p + \frac{K_i}{s})  G(s)}{1 + (K_p + \frac{K_i}{s})  G(s)}$

### Cálculo de $K_p$ y $K_i$

Para calcular $K_p$ y $K_i$, se necesitan criterios de diseño como el tiempo de asentamiento, el sobrepaso máximo, la constante de tiempo, etc. Sin criterios específicos, no podemos determinar valores únicos para $K_p$ y $K_i$. Sin embargo, podemos establecer las ecuaciones de implementación basándonos en los principios generales del control.

#### Implementación

1. **Para el Controlador Proporcional (P):** Selecciona un valor de $K_p$ basado en los criterios de diseño deseados (p.ej., tiempo de respuesta, estabilidad, error en estado estacionario). Ajusta $K_p$ para lograr el comportamiento deseado.

2. **Para el Controlador Proporcional-Integral (PI):** Selecciona valores para $K_p$ y $K_i$. Generalmente, $K_p$ ajusta la rapidez de la respuesta del sistema y $K_i$ elimina el error en estado estacionario. Usa métodos como el de Ziegler-Nichols, Cohen-Coon, o prueba y error para encontrar estos valores.

Si deseas, puedo mostrarte cómo establecer un proceso de diseño o estimación de valores para $K_p$ y $K_i$ utilizando métodos estándar, aunque los valores específicos dependerán de los criterios de desempeño que elijas.
