# Características de Variables Aleatorias: Explicación Detallada

## 1. Introducción a las Características de Variables Aleatorias

Las características de variables aleatorias son valores numéricos que nos permiten resumir y entender el comportamiento probabilístico de estas variables. Como menciona Vanlesberg en las notas: "Existen una serie de números que resumen las características dominantes del comportamiento de una variable aleatoria."

Estas características se clasifican en:

- Medidas de tendencia central
- Medidas de variabilidad
- Medidas de forma (asimetría y curtosis)

Entender estas características es fundamental porque nos permiten trabajar con modelos probabilísticos simplificados en lugar de tener que usar las funciones de probabilidad o densidad completas.

## 2. Medidas de Tendencia Central

### 2.1 Esperanza Matemática (Media)

La esperanza matemática representa el valor promedio o centro de masa de la distribución.

**Para variables discretas:** $E(X) = \sum_{i} x_i \cdot P(X = x_i)$

**Para variables continuas:** $E(X) = \int_{-\infty}^{\infty} x \cdot f(x) , dx$

#### Propiedades de la Esperanza:

1. $E(c) = c$ donde $c$ es una constante
2. $E(cX) = c \cdot E(X)$
3. $E(X + Y) = E(X) + E(Y)$
4. Si $X$ e $Y$ son independientes, entonces $E(XY) = E(X) \cdot E(Y)$

**Ejemplo (Ejercicio 1 de la guía):** En el ejercicio 1, tenemos una variable aleatoria $X$ que representa el porcentaje de contaminante con densidad: $f(x) = \begin{cases} a + bx^2 & \text{para } 0 \leq x \leq 1 \ 0 & \text{en otro caso} \end{cases}$

Sabemos que $E(X) = 3/5$. Este valor nos indica el porcentaje promedio de contaminante que podemos esperar encontrar en una muestra.

**Ejemplo (Ejercicio 2 de la guía):** La producción de trigo $X$ (en miles de toneladas) tiene función de densidad: $f(x) = \begin{cases} \frac{3}{22}(x + 3)(2 - x) & \text{para } 0 \leq x \leq 2 \ 0 & \text{en otro caso} \end{cases}$

El beneficio es $B = 5000X - 1000$. Para calcular el beneficio esperado, usaríamos: $E(B) = E(5000X - 1000) = 5000 \cdot E(X) - 1000$

### 2.2 Mediana

La mediana es el valor que divide la distribución en dos partes iguales en términos de probabilidad.

**Para variables discretas:** Es el valor $x_m$ tal que $P(X \leq x_m) \geq 0.5$ y $P(X \geq x_m) \geq 0.5$

**Para variables continuas:** Es el valor $x_m$ tal que $\int_{-\infty}^{x_m} f(x) , dx = 0.5$

### 2.3 Cuantiles

Los cuantiles dividen la distribución en partes con igual probabilidad:

- Cuartiles: dividen en 4
- Deciles: dividen en 10
- Percentiles: dividen en 100

El cuantil de orden $p$ (donde $p \in [0,1]$) es el valor $X_p$ que cumple:

- Para discretas: $P(X \leq X_p) \geq p$ y $P(X < X_p) \leq p$
- Para continuas: $\int_{-\infty}^{X_p} f(x) , dx = p$

### 2.4 Modo

El modo es el valor de la variable aleatoria con mayor probabilidad de ocurrencia:

- Para discretas: el valor con mayor probabilidad
- Para continuas: el punto donde la función de densidad alcanza su máximo

**Ejemplo (Ejercicio 4 de la guía):** La variable "cantidad de días con precipitación ≥ 80mm en una semana" tiene distribución:

|x|0|1|2|
|---|---|---|---|
|f(x)|0.1|0.3|0.6|

El modo es x = 2 (valor con mayor probabilidad), lo que nos indica que es más probable tener 2 días con alta precipitación que cualquier otra cantidad.

## 3. Momentos de Variables Aleatorias

Los momentos son una forma sistemática de caracterizar distribuciones de probabilidad.

### 3.1 Momentos No Centrados

El momento no centrado de orden $r$ se define como:

**Para variables discretas:** $\mu'_r = E(X^r) = \sum_{i} x_i^r \cdot P(X = x_i)$

**Para variables continuas:** $\mu'_r = E(X^r) = \int_{-\infty}^{\infty} x^r \cdot f(x) , dx$

El momento de orden 1 ($\mu'_1$) corresponde a la media o esperanza matemática.

### 3.2 Momentos Centrados

Los momentos centrados se calculan respecto a la media:

**Para variables discretas:** $\mu_r = E[(X - \mu)^r] = \sum_{i} (x_i - \mu)^r \cdot P(X = x_i)$

**Para variables continuas:** $\mu_r = E[(X - \mu)^r] = \int_{-\infty}^{\infty} (x - \mu)^r \cdot f(x) , dx$

El momento centrado de orden 2 ($\mu_2$) corresponde a la varianza.

## 4. Medidas de Variabilidad

### 4.1 Varianza y Desviación Estándar

La varianza mide la dispersión de los valores respecto a la media:

$Var(X) = \sigma^2 = E[(X - \mu)^2] = E(X^2) - [E(X)]^2$

La desviación estándar es $\sigma = \sqrt{Var(X)}$

#### Propiedades de la Varianza:

1. $Var(c) = 0$ donde $c$ es una constante
2. $Var(cX) = c^2 \cdot Var(X)$
3. $Var(X + Y) = Var(X) + Var(Y) + 2 \cdot Cov(X,Y)$
4. Si $X$ e $Y$ son independientes, entonces $Var(X + Y) = Var(X) + Var(Y)$

**Ejemplo (Ejercicio 10 de la guía):** El nivel de agua de un tanque (en metros) es una variable aleatoria $X$ con densidad: $f(x) = \begin{cases} 6x(1 - x) & \text{para } 0 \leq x \leq 1 \ 0 & \text{en otro caso} \end{cases}$

Para calcular la varianza, primero encontramos $E(X)$ y $E(X^2)$:

- $E(X) = \int_{0}^{1} x \cdot 6x(1-x) , dx$
- $E(X^2) = \int_{0}^{1} x^2 \cdot 6x(1-x) , dx$
- $Var(X) = E(X^2) - [E(X)]^2$

La varianza nos indicaría qué tan variable es el nivel del agua en el tanque.

### 4.2 Coeficiente de Variación

El coeficiente de variación es una medida relativa de dispersión:

$CV = \frac{\sigma}{\mu} \cdot 100$

Es útil para comparar la variabilidad entre distribuciones con diferentes unidades o magnitudes.
### 4.3 Teorema de Tchebycheff

El teorema de Tchebycheff proporciona límites para la probabilidad de que una variable aleatoria se desvíe de su media en más de $k$ desviaciones estándar:

$P(|X - \mu| \geq k\sigma) \leq \frac{1}{k^2}$

O equivalentemente:

$P(|X - \mu| < k\sigma) \geq 1 - \frac{1}{k^2}$

**Ejemplo (Ejercicio 3 de la guía):** El tiempo para transportar un cargamento entre dos puertos tiene media 90 horas y desviación 3 horas. Si el capitán quiere llegar entre 80 y 100 horas, aplicando Tchebycheff:

$P(|X - 90| < 10) = P(80 < X < 100)$ $k = \frac{10}{3} \approx 3.33$ $P(|X - \mu| < k\sigma) \geq 1 - \frac{1}{k^2} \geq 1 - \frac{1}{(10/3)^2} \geq 1 - \frac{9}{100} = 0.91$

Por tanto, la probabilidad de que el barco llegue entre 80 y 100 horas es al menos 0.91 (o 91%).

**Ejemplo (Ejercicio 19 de la guía):** Para la VA del ejercicio 10, nos piden calcular: a) $P(0.06 \leq X \leq 0.94)$ b) $P(0.17 \leq X \leq 0.83)$

Y verificar si son coherentes con el teorema de Tchebycheff.

## 5. Medidas de Forma

### 5.1 Asimetría (Skewness)

La asimetría mide la falta de simetría en una distribución. Se calcula mediante el momento centrado de orden 3 normalizado:

$\gamma_1 = \frac{\mu_3}{\sigma^3}$

- Si $\gamma_1 = 0$: distribución simétrica
- Si $\gamma_1 > 0$: asimetría positiva (cola derecha más larga)
- Si $\gamma_1 < 0$: asimetría negativa (cola izquierda más larga)

### 5.2 Curtosis

La curtosis mide el "apuntamiento" o concentración de valores alrededor de la media:

$\gamma_2 = \frac{\mu_4}{\sigma^4} - 3$

- Si $\gamma_2 = 0$: mesocúrtica (como la normal)
- Si $\gamma_2 > 0$: leptocúrtica (más apuntada que la normal)
- Si $\gamma_2 < 0$: platicúrtica (más achatada que la normal)

## 6. Características de Variables Aleatorias Conjuntas

### 6.1 Distribución Conjunta

Para variables bidimensionales $(X,Y)$, la distribución conjunta puede ser:

**Discreta:** $P(X=x_i, Y=y_j) = f(x_i, y_j)$

**Continua:** $f(x,y)$ donde $\iint f(x,y) , dx , dy = 1$

### 6.2 Esperanzas Marginales

Las esperanzas marginales son las esperanzas de cada variable individualmente:

**Esperanza marginal de X:** $E(X) = \iint x \cdot f(x,y) , dx , dy = \int x \cdot f_X(x) , dx$

**Esperanza marginal de Y:** $E(Y) = \iint y \cdot f(x,y) , dx , dy = \int y \cdot f_Y(y) , dy$

### 6.3 Varianzas Marginales

Las varianzas marginales son las varianzas de cada variable individualmente:

$Var(X) = E(X^2) - [E(X)]^2$ $Var(Y) = E(Y^2) - [E(Y)]^2$

### 6.4 Covarianza

La covarianza mide la relación lineal entre dos variables aleatorias:

$Cov(X,Y) = E[(X - E(X))(Y - E(Y))] = E(XY) - E(X) \cdot E(Y)$

- Si $Cov(X,Y) > 0$: relación lineal positiva
- Si $Cov(X,Y) < 0$: relación lineal negativa
- Si $Cov(X,Y) = 0$: no hay relación lineal (pero puede haber otro tipo de relación)

**Ejemplo (Ejercicio 16 de la guía):** Para los tiempos de llegada $(X)$ y de ingreso $(Y)$ al sistema con densidad conjunta: $f(x,y) = \begin{cases} \frac{2}{3}(x + 2y) & \text{si } 0 \leq x \leq 1, 0 \leq y \leq 1 \ 0 & \text{en cualquier otro caso} \end{cases}$

La covarianza nos indicaría si hay relación entre el tiempo de llegada y el tiempo de ingreso.

### 6.5 Coeficiente de Correlación

El coeficiente de correlación normaliza la covarianza para obtener un valor entre -1 y 1:

$\rho_{XY} = \frac{Cov(X,Y)}{\sigma_X \cdot \sigma_Y}$

- Si $\rho_{XY} = 1$: correlación positiva perfecta
- Si $\rho_{XY} = -1$: correlación negativa perfecta
- Si $\rho_{XY} = 0$: no hay correlación lineal

### 6.6 Independencia

Dos variables son independientes si y solo si: $f(x,y) = f_X(x) \cdot f_Y(y)$

Si $X$ e $Y$ son independientes, entonces $Cov(X,Y) = 0$ (pero la inversa no siempre es cierta).

**Ejemplo (Ejercicio 8 de la guía):** Las variables $X$ (número de fallos) e $Y$ (número de llamadas al técnico) tienen distribución conjunta:

|f(x,y)|x=1|x=2|x=3|
|---|---|---|---|
|y=1|0.05|0.05|0.10|
|y=2|0.05|0.10|0.35|
|y=3|0.00|0.20|0.10|

Calculando la covarianza podemos determinar si hay relación entre el número de fallos y las llamadas al técnico.

### 6.7 Suma de Variables Aleatorias

Para dos variables aleatorias $X$ e $Y$:

$E(X + Y) = E(X) + E(Y)$

Si $X$ e $Y$ son independientes: $Var(X + Y) = Var(X) + Var(Y)$

En general: $Var(X + Y) = Var(X) + Var(Y) + 2 \cdot Cov(X,Y)$

**Ejemplo (Ejercicio 18 de la guía):** Tenemos dos dispositivos de inspección $X$ e $Y$ con: $E(X^2) = 5$, $V(X) = 4$, $V(X + Y) = 10$, $Cov(X,Y) = 2$

Podemos encontrar $E(X)$ usando $V(X) = E(X^2) - [E(X)]^2$: $4 = 5 - [E(X)]^2$, por lo tanto $E(X) = 1$

Y también $V(Y)$ usando $V(X + Y) = V(X) + V(Y) + 2Cov(X,Y)$: $10 = 4 + V(Y) + 2(2)$, por lo tanto $V(Y) = 2$

## Conclusión

Entender las características de las variables aleatorias es fundamental para modelar y analizar fenómenos aleatorios. Estos conceptos te permitirán resolver los ejercicios de la guía con mayor facilidad, ya que ahora puedes:

1. Calcular e interpretar medidas de tendencia central
2. Analizar la variabilidad de distribuciones
3. Evaluar la forma de las distribuciones mediante asimetría y curtosis
4. Estudiar relaciones entre variables aleatorias mediante covarianza y correlación
5. Aplicar propiedades para la suma y transformación de variables aleatorias

Al abordar los ejercicios, recuerda seguir estos pasos:

1. Identificar el tipo de variable (discreta/continua)
2. Verificar que la función sea válida (no negativa y suma/integral = 1)
3. Calcular las características solicitadas aplicando las fórmulas correctas
4. Interpretar los resultados en el contexto del problema