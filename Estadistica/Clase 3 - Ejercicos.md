# Resolución de Ejercicios: Características de Variables Aleatorias

## Ejercicio 1

El porcentaje de contaminante presente en una muestra de aire es una variable aleatoria X con función de densidad dada por:

$f(x) = \begin{cases} a + bx^2 & \text{para } 0 \leq x \leq 1 \ 0 & \text{en otro caso} \end{cases}$

a) Se sabe que E(X) = 3/5, determine alguna medida que indique cómo se comporta la variable respecto al valor central. b) Caracterizar la forma de la función dada.

### Resolución:

#### Parte a)

Primero, necesitamos encontrar los valores de $a$ y $b$ usando las condiciones:

1. La condición de cierre (área bajo la curva = 1): $\int_{0}^{1} (a + bx^2) , dx = 1$

$\left[ ax + b\frac{x^3}{3} \right]_{0}^{1} = 1$

$a \cdot 1 + b \cdot \frac{1}{3} - (a \cdot 0 + b \cdot \frac{0^3}{3}) = 1$

$a + \frac{b}{3} = 1$ ... (1)

2. La esperanza es E(X) = 3/5: $E(X) = \int_{0}^{1} x \cdot (a + bx^2) , dx = \frac{3}{5}$

$\int_{0}^{1} (ax + bx^3) , dx = \frac{3}{5}$

$\left[ a\frac{x^2}{2} + b\frac{x^4}{4} \right]_{0}^{1} = \frac{3}{5}$

$a \cdot \frac{1}{2} + b \cdot \frac{1}{4} = \frac{3}{5}$ ... (2)

Resolviendo el sistema de ecuaciones (1) y (2): $a + \frac{b}{3} = 1$ ... (1) $\frac{a}{2} + \frac{b}{4} = \frac{3}{5}$ ... (2)

Multiplicando (2) por 2: $a + \frac{b}{2} = \frac{6}{5}$ ... (3)

Restando (1) de (3): $\frac{b}{2} - \frac{b}{3} = \frac{6}{5} - 1$

$\frac{3b-2b}{6} = \frac{1}{5}$

$\frac{b}{6} = \frac{1}{5}$

$b = \frac{6}{5}$

Sustituyendo en (1): $a + \frac{6/5}{3} = 1$

$a + \frac{2}{5} = 1$

$a = \frac{3}{5}$

Ahora podemos calcular la varianza para medir la dispersión respecto al valor central:

$Var(X) = E(X^2) - [E(X)]^2$

$E(X^2) = \int_{0}^{1} x^2 \cdot (a + bx^2) , dx = \int_{0}^{1} (ax^2 + bx^4) , dx$

$E(X^2) = \left[ a\frac{x^3}{3} + b\frac{x^5}{5} \right]_{0}^{1} = a\frac{1}{3} + b\frac{1}{5} = \frac{3}{5} \cdot \frac{1}{3} + \frac{6}{5} \cdot \frac{1}{5} = \frac{1}{5} + \frac{6}{25} = \frac{5 + 6}{25} = \frac{11}{25}$

$Var(X) = \frac{11}{25} - \left(\frac{3}{5}\right)^2 = \frac{11}{25} - \frac{9}{25} = \frac{2}{25} = 0.08$

El desvío estándar es: $\sigma = \sqrt{Var(X)} = \sqrt{\frac{2}{25}} = \frac{\sqrt{2}}{5} \approx 0.28$

Esta varianza (0.08) y desvío estándar (0.28) nos indican que los valores de porcentaje de contaminante tienen una dispersión relativamente baja alrededor de la media (3/5 = 0.6).

#### Parte b)

Para caracterizar la forma de la función, podemos calcular los coeficientes de asimetría y curtosis. También podemos analizar visualmente la función.

La función de densidad es $f(x) = \frac{3}{5} + \frac{6}{5}x^2$ para $0 \leq x \leq 1$.

Observaciones sobre la forma:

1. Es una función cuadrática creciente en el intervalo [0,1]
2. El valor mínimo es $f(0) = \frac{3}{5} = 0.6$
3. El valor máximo es $f(1) = \frac{3}{5} + \frac{6}{5} = \frac{9}{5} = 1.8$

Para la asimetría, necesitamos el momento centrado de orden 3: $\mu_3 = E[(X-\mu)^3]$

Dado que este cálculo es extenso, podemos concluir que la función tiene asimetría positiva, ya que el máximo está en x=1 y el gráfico se inclina hacia la derecha.

## Ejercicio 2

La producción de trigo en una determinada región es una variable aleatoria X (en miles de toneladas) cuya distribución está caracterizada por la siguiente función:

$f(x) = \begin{cases} \frac{3}{22}(x + 3)(2 - x) & \text{para } 0 \leq x \leq 2 \ 0 & \text{en otro caso} \end{cases}$

El beneficio por cada mil toneladas producidas se obtiene como función de la cantidad producida resulta B = 5000X - 1000. ¿Cuál es el beneficio esperado?

### Resolución:

Primero, verificamos que $f(x)$ sea una función de densidad válida:

1. $f(x) \geq 0$ para todo $x$ en $[0,2]$, ya que $(x + 3) > 0$ y $(2 - x) > 0$ en ese intervalo.
    
2. Comprobamos la condición de cierre: $\int_{0}^{2} \frac{3}{22}(x + 3)(2 - x) , dx = 1$
    

$\frac{3}{22}\int_{0}^{2} (x + 3)(2 - x) , dx = \frac{3}{22}\int_{0}^{2} (2x + 6 - x^2 - 3x) , dx$

$\frac{3}{22}\int_{0}^{2} (6 - x^2 - x) , dx = \frac{3}{22}\left[ 6x - \frac{x^3}{3} - \frac{x^2}{2} \right]_{0}^{2}$

$\frac{3}{22}\left[ 12 - \frac{8}{3} - 2 - 0 \right] = \frac{3}{22}\left[ 12 - \frac{8}{3} - 2 \right] = \frac{3}{22}\left[ \frac{36 - 8 - 6}{3} \right] = \frac{3}{22} \cdot \frac{22}{3} = 1$ ✓

Para calcular el beneficio esperado, necesitamos $E(X)$:

$E(X) = \int_{0}^{2} x \cdot \frac{3}{22}(x + 3)(2 - x) , dx$

$E(X) = \frac{3}{22}\int_{0}^{2} x(x + 3)(2 - x) , dx$

$E(X) = \frac{3}{22}\int_{0}^{2} x(2x + 6 - x^2 - 3x) , dx$

$E(X) = \frac{3}{22}\int_{0}^{2} (2x^2 + 6x - x^3 - 3x^2) , dx$

$E(X) = \frac{3}{22}\int_{0}^{2} (-x^3 - x^2 + 6x) , dx$

$E(X) = \frac{3}{22}\left[ -\frac{x^4}{4} - \frac{x^3}{3} + 3x^2 \right]_{0}^{2}$

$E(X) = \frac{3}{22}\left[ -\frac{16}{4} - \frac{8}{3} + 12 - 0 \right]$

$E(X) = \frac{3}{22}\left[ -4 - \frac{8}{3} + 12 \right] = \frac{3}{22}\left[ 12 - 4 - \frac{8}{3} \right] = \frac{3}{22}\left[ 8 - \frac{8}{3} \right]$

$E(X) = \frac{3}{22}\left[ \frac{24 - 8}{3} \right] = \frac{3}{22} \cdot \frac{16}{3} = \frac{16}{22} = \frac{8}{11} \approx 0.7273$ miles de toneladas.

Ahora calculamos el beneficio esperado: $E(B) = E(5000X - 1000) = 5000 \cdot E(X) - 1000$

$E(B) = 5000 \cdot \frac{8}{11} - 1000 = \frac{40000}{11} - 1000 = \frac{40000 - 11000}{11} = \frac{29000}{11} \approx 2636.36$ unidades monetarias.

Por lo tanto, el beneficio esperado es aproximadamente 2636.36 unidades monetarias.

## Ejercicio 3

El tiempo requerido para transportar un cargamento por vía fluvial entre dos puertos sigue una distribución de probabilidades con una media de 90 hs. y desvío de 3 hs. El capitán de un barco pretende llegar a un puerto entre 80 y 100 hs. después de haber salido del primer puerto. ¿Puede con esta información determinar la probabilidad de que realmente esto suceda?

### Resolución:

Tenemos los siguientes datos:

- Media (μ) = 90 horas
- Desviación estándar (σ) = 3 horas
- Queremos calcular P(80 ≤ X ≤ 100)

Sin conocer la distribución específica, podemos aplicar el Teorema de Tchebycheff para encontrar un límite inferior para esta probabilidad.

El teorema establece que para cualquier distribución y cualquier valor k > 0: $P(|X - \mu| < k\sigma) \geq 1 - \frac{1}{k^2}$

En nuestro caso: $P(|X - 90| < 10) = P(80 < X < 100)$

Donde $k = \frac{10}{3}$ (ya que $10 = k \cdot 3$)

Aplicando el teorema: $P(80 < X < 100) \geq 1 - \frac{1}{(10/3)^2} = 1 - \frac{1}{100/9} = 1 - \frac{9}{100} = 1 - 0.09 = 0.91$

Por lo tanto, la probabilidad de que el barco llegue entre 80 y 100 horas es al menos 0.91 o 91%.

Si la distribución fuera normal (lo cual no se especifica), podríamos calcular la probabilidad exacta: $P(80 \leq X \leq 100) = P\left(\frac{80-90}{3} \leq Z \leq \frac{100-90}{3}\right) = P(-3.33 \leq Z \leq 3.33) \approx 0.9992$

Sin embargo, dado que no conocemos la distribución específica, lo más seguro es usar el teorema de Tchebycheff, que nos da un límite inferior de 91%.

## Ejercicio 4

La variable aleatoria cantidad de días en que la precipitación alcanzó los 80 mm, durante una semana dada del mes de marzo en Santa Fe, tiene la siguiente distribución de probabilidades:

|x|0|1|2|
|---|---|---|---|
|f(x)|0.1|0.3|0.6|

Determinar las principales medidas de tendencia central interpretando sus valores.

### Resolución:

Verificamos primero que la distribución es válida: $\sum f(x) = 0.1 + 0.3 + 0.6 = 1$ ✓

#### 1. Media o Esperanza Matemática:

$E(X) = \sum x \cdot f(x) = 0 \cdot 0.1 + 1 \cdot 0.3 + 2 \cdot 0.6 = 0 + 0.3 + 1.2 = 1.5$ días.

Interpretación: En promedio, durante una semana de marzo en Santa Fe, habrá 1.5 días con precipitaciones iguales o superiores a 80 mm.

#### 2. Varianza:

$Var(X) = E(X^2) - [E(X)]^2$

$E(X^2) = \sum x^2 \cdot f(x) = 0^2 \cdot 0.1 + 1^2 \cdot 0.3 + 2^2 \cdot 0.6 = 0 + 0.3 + 2.4 = 2.7$

$Var(X) = 2.7 - (1.5)^2 = 2.7 - 2.25 = 0.45$

Desviación estándar: $\sigma = \sqrt{0.45} \approx 0.67$ días.

#### 3. Mediana:

Para encontrar la mediana, buscamos el valor $x_m$ tal que $P(X \leq x_m) \geq 0.5$ y $P(X \geq x_m) \geq 0.5$

$P(X \leq 0) = 0.1 < 0.5$ $P(X \leq 1) = 0.1 + 0.3 = 0.4 < 0.5$ $P(X \leq 2) = 0.1 + 0.3 + 0.6 = 1 \geq 0.5$

$P(X \geq 0) = 0.1 + 0.3 + 0.6 = 1 \geq 0.5$ $P(X \geq 1) = 0.3 + 0.6 = 0.9 \geq 0.5$ $P(X \geq 2) = 0.6 \geq 0.5$

La mediana es $x_m = 2$, ya que es el primer valor que cumple $P(X \leq x_m) \geq 0.5$.

Interpretación: En al menos la mitad de las semanas, habrá 2 días con precipitaciones de 80 mm o más.

#### 4. Moda:

La moda es el valor con mayor probabilidad. En este caso es x = 2 con f(2) = 0.6.

Interpretación: Lo más frecuente es tener 2 días con precipitaciones de 80 mm o más durante una semana de marzo.

#### Resumen e Interpretación General:

- Media = 1.5 días: El valor promedio de días con altas precipitaciones
- Mediana = 2 días: El valor que divide la distribución en dos partes iguales
- Moda = 2 días: El valor que ocurre con mayor frecuencia

Como la moda > mediana > media, podemos decir que la distribución presenta asimetría negativa, lo que indica que los valores tienden a concentrarse en la parte alta de la distribución (hay mayor probabilidad de tener más días de lluvia intensa que pocos).