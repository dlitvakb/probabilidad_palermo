# Distribuciones de Probabilidad

Es una tabla o un grafico que relaciona los valores de una variable aleatoria con su probabilidad de ocurrencia.

## Variable Aleatoria

Una regla bien definida que asigna un valor numerico a cada resultado posible de un experimento aleatorio

* Discretas: Toman valores numerables (coinciden con los enteros)
* Continuas: Toman valores no numerables (Reales)

## Distribuciones para Variables Discretas

### Formas de obtener probabilidades

* Experimental
* Teorica: Una funcion que describe el comportamiento

### Axiomas

* Las probabilidades puntuales deben ser >= 0
* La sumatoria de las probabilidades == 1

### Probabilidad Acumulada

```
         Xa
 F(Xa) = Σ(P(Xi))     # Probabilidad Acumulada Izquierda
         0

 G(Xa) = 1 - F(Xa)      # Probabilidad Acumulada Derecha
```

### Tendencia

* Valor Esperado (Esperanza): Media Aritmetica como resultado de infinitas pruebas `E(x) = Σ(Xi * P(Xi))`
* Variabilidad: `σ**2 X = Σ((Xi - E(X))**2 * P(Xi))`
* Desvio: `σ = Sqrt(σ**2)`
* Moda: Valor de la variable mas probable


### Modelo Binomial

* Proceso Bernoulli: Experimento con 2 resultados excluyentes y una `P(Exito)` conocida

Suponga un experimento aleatorio con 2 resultados posibles, los cuales son clasificados como `Exito` y `Fracaso`
Dichos resultados son **Excluyentes**. `P(Exito)` es conocida.

Se realizan pruebas repetidas, cuyos resultados son independientes => `P(Exito) = cte`

Se genera una Variable de Interes: `X = nro de exitos en N pruebas`

* `X` es una Variable Aleatoria Discreta
* `0 <= X <= n`

* Formula Binomial: `Pbi(X=x/n;p) = nCx * p**x * (1 - p)**(n-x)`
* Esperanza: `E(X) = n * p`
* Varianza: `σ**2(X) = n * p * q` - `q = (1 - p)`
* Desvio: `σ(X) = Sqrt(n * p * q)`

> `nCx = n! / (x! * (n - x)!)`

Graficamente:
* Asimetrica Positiva -> `p < 0.5`
* Asimetrica Negativa -> `p > 0.5`
* Simetrica -> `p = 0.5` o `0.1 <= p <= 0.9 ^ n grande`

#### Ejemplo

```
En una fabrica de ensaladeras, se realiza un control de calidad para ver si
el producto es `Bueno` o `Defectuoso`. `Defectuoso => Exito`

* `P(Defecto) = 0.15`

Resultado | r | P(r)
----------|---|------
Buena     | 0 | 0.85
Defectuosa| 1 | 0.15

X = nro de ensaladeras defectuosas en set (3 ensaladeras) = r1 + r2 + r3

 X | P(X)
 0 | P(bue) ** 3 = 0.614125
 1 | 3 * P(def) * P(bue) ** 2 = 0.325125
 2 | 3 * P(def) ** 2 * P(bue) = 0.057375
 3 | P(def) ** 3 = 0.003375

E(X) = 3 * 0.15 = 0.45

P(X = 4D en 12) = 12C4 * P(def)**4 * P(bue)**(12-4) = 0.06828
```

### Modelo Poisson

> `~Po(ƛ = b.t)`
> X es una V.A.D.
> `0 <= X <= ∞`

* X: Nro ocurrencias en un continuo de tiempo o espacio
* ƛ: Frecuencia media del suceso en la extension t del continuo
* b: Frecuencia media del suceso en una unidad del continuo
* t: Cierta extension del continuo

* Formula Poisson: `Ppo(X/ƛ) = (e**-ƛ * ƛ**X) / X!`
* Esperanza: `E(X) = ƛ`
* Varianza: `σ**2(X) = ƛ`
* Desvio: `σ(X) = Sqrt(ƛ)`

Graficamente:
* Asimetrica Positiva -> `ƛ < 20`
* Simetrica -> `ƛ > 20`

Condiciones:
* El suceso debe ocurrir en forma instantanea
* Las ocurrencias deben producirse en forma independiente
* La probabilidad de que ocurra el suceso debe ser la misma para
  extensiones del continuo del mismo tamaño, cualquiera sea su ubicacion

> La ocurrencia del suceso se debe presentar de forma individual y colectivamente
> al azar en el continuo.


#### Ejemplo

```
X = nro clientes por hora
b = 15cl/Hora
t = 10min
ƛ = (15/60) * 10 = 2.5
```

