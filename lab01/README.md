## **INTRODUCCIÓN**

**Etapa 1: Planteamiento del problema de control**

**¿Qué?**

Diseñar un sistema que **sea capaz de mantener** la posición de la copa de un puente grúa dentro de los parámetros deseados, sin modificar el valor de la velocidad de giro ("X rpm").

**¿Cómo?**

Utilizar un potenciómetro como entrada del sistema de control.

**¿Para qué?**

Para que el motor mantenga una velocidad constante y la copa del puente grúa se posicione de forma precisa.

**¿Cómo abordar un problema de control?**

Para poder desarrollar un problema de control se pueden seguir como guía los siguientes pasos:

1. **Definir el problema de control:**
    * ¿Qué señales y variables están involucradas?
    * ¿Cuál es el objetivo de control?
    * ¿Qué tipo de controlador se utilizará?
    * ¿Qué herramientas se necesitan?

2. **Entender la planta:**
    * Estudiar el modelo dinámico y sus características (exploración matemática así como el hardware a utilizar: código, motores, entre otros).
    * Definir la planta: otorgarle un valor a los parámetros de la planta o en caso que no sea posible realizar experimentos para obtener un aproximado.

3. **Diseño y simulación:**
    * Aplicar la teoría de diseño sobre la planta para verificar su funcionamiento.
    * Implementar y probar: evaluar en experimentación el comportamiento del sistema.

**Etapa 2: Planteamiento del problema de control**

Para un buen planteamiento del problema se deben seguir ciertos pasos para así lograr realizarlo de una forma satisfactoria. Para explicar este procedimiento se utilizará el siguiente ejemplo:

**Ejemplo:**

Consideremos un motor con un brazo acoplado. Mediante un voltaje aplicado al motor este hace girar el brazo.

**Objetivo del controlador:**

Se define la variable a controlar (en este caso puede ser un control de posición o de velocidad) y cómo se quiere llegar a la referencia, esto último pueden ser características deseadas de la respuesta temporal del lazo cerrado (T33).

**Definir min 3 características de esta respuesta:**

* **Sobrepico**
* **Tiempo de aventamiento**
* **Error en estado estacionario (Ep) = error en posición**

**Señales y sistemas:**

Definir físicamente el origen de las señales y sistemas que conforman el lazo cerrado.

**Ejemplo:**

* **Sensor de posición:** Mide la posición actual del brazo.
* **Controlador:** Calcula la señal de control para el motor.
* **Motor:** Convierte la señal de control en movimiento.
* **Brazo:** Se mueve de acuerdo a la velocidad del motor.

**Planta:**

El conjunto formado por el motor y el brazo.

**Objetivo:**

Diseñar un controlador que haga que la posición del brazo siga una referencia deseada.

**Consideraciones:**

* La velocidad del motor no se puede modificar.
* Se debe utilizar un potenciómetro como entrada del sistema de control.

**Próximos pasos:**

* Modelar la planta.
* Diseñar un controlador.
* Simular el sistema.
* Implementar el sistema.
* Probar el sistema.

**Planta (G):**

* Conjunto de elementos que componen el sistema a controlar.
* Se le asocian 2 señales: entrada (u) y salida (y).
* Se puede ver de la siguiente forma:

**Referencia (r):**

* Sirve para darle una "forma" o valor al objetivo del controlador (por ejemplo, mantener el brazo a X°).
* Esto también conlleva la introducción de una señal de realimentación en el sistema con el fin de poder comparar la posición actual y la referencia.
* Esta comparación se realiza mediante una resta cuyo resultado denominamos error (e).

**Error (e):**

* Valor que se debe corregir por medio del controlador para acercarse a la referencia.

**Sensor (H):**

* Es un sistema que nos permite conocer la salida de la planta.
* Se intenta que su función de transferencia se acerque a 1 lo más posible mediante el uso de filtros y otros elementos.

**Control (C):**

* Un sistema dinámico que regula la entrada de la planta con el fin de que la salida sea lo más parecida a la referencia y así hacer tender el error a cero.
* También se encarga de la conversión de datos.

**Perturbación (d):**

* Es una entrada a la planta que modifica la salida, esta no se puede predecir.

**Evaluación del desempeño del controlador:**

* **Desempeño:** La capacidad del controlador de rechazar perturbaciones (regresar a la referencia).
* **Robustez:** Mantener la estabilidad del sistema de lazo cerrado a pesar de la incertidumbre.

**Elementos del diagrama:**

* **Entrada (u):** Voltaje, torque o posición.
* **Salida (y):** Posición.
* **Referencia (r):** Posición deseada.
* **Planta (G):** Sistema a controlar.
* **Sensor (H):** Sensor de posición.
* **Control (C):** Controlador.
* **Error (e):** Diferencia entre la referencia y la salida.
* **Perturbación (d):** Entrada no deseada que afecta la salida.
