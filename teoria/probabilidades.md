# Probabilidades

> La probabilidad es una medida de incertidumbre.

## Enfoque de Laplace -> Teorico

> Si un experimento aleatorio admite `n` resultados, todos igualmente probables, `f` de los cuales
> son favorables a la ocurrencia de un suceso `A`. Se define a la Probabilidad de A como el cociente entre
> casos favorables y casos posibles.
> `P(A) = f/n`

> Para que Laplace funcione, se DEBE garantizar la equiprobabilidad

* Experimento Aleatorio: experimento cuyos resultados son, mas o menos, imprevisibles.

## Enfoque de la Probabilidad Frecuentista -> Empirico

> La probabilidad de un suceso `P(A) = Lim(n -> N) frel(A)` `N = Tamanio total poblacion o infinito`

> Las frecuencias relativas son estimaciones de las probabilidades

```
  Cand | fabs | frel = f/n | %
    A  |  120 |     0,6    | 60
    B  |   60 |     0,3    | 30
    C  |   20 |     0,1    | 10
  --------------------------------
   Total: 200
```

### Ley de los grandes numeros

A medida que aumenta el numero de ensayos, la frecuencia relativa de un resultado de un experimento
converge estocasticamente hacia un numero que es la verdadera probabilidad

## Enfoque Axiomatico de Kolmogorov

> Una probabilidad es una funcion de conjunto que asocia un valor numerico no negativo a cada
> resultado de un experimento aleatorio.
> Una probabilidad cumple con los siguientes axiomas:
>  - La probabilidad es un numero no negativo `P(A) >= 0`
>  - La probabilidad del espacio muestral es siempre igual a 1 `P(espacio muestral) = 1`
>  - La probabilidad de 2 sucesos excluyentes es igual a la suma
>    de sus probabilidades individuales `P(A v B) = P(A) + P(B)`
>
>  => `0 <= P(A) <= 1`

* Probabilidades iguales a 0 => Imposibles o Casi Imposibles
* Probabilidades cercanas a 0 => Suceso raro
* Probabilidad 1 => Certeza
* Probabilidad 0.5 => Incertidumbre Absoluta

* Espacio Muestral: Rodos los resultados posibles
* Punto Muestral: Un resultado posible
* Suceso/Evento: Un Punto Muestral, o conjunto de Puntos, que resultan de interes

```
  Tipos de       | Reglas de
  Suceso         | Calculo
---------------------------
  Excluyentes    | Suma     # Expresion general: P(A v B) = P(A) + P(B) - P(A ^ B)
  No Excluyentes | Suma     #     en Excluyentes: P(A ^ B) = 0
  Independientes | Producto # Expresion general: P(A ^ B) = P(A) * P(B/A)
  Dependientes   | Producto #     La inversa es equivalente
```

1. Sucesos Excluyentes: Sucesos que no pueden ocurrir juntos en la misma prueba
2. Sucesos No Excluyentes: Sucesos que pueden ocurrir juntos en la misma prueba
3. Sucesos Independientes: Sucesos en que la ocurrencia de otro Suceso no modifica
                           la probabilidad de ocurrencia del mismo
4. Sucesos Dependientes: Sucesos en que la ocurrencia de otro Suceso modifica
                         la probabilidad de ocurrencia del mismo
5. Sucesos Complementarios: `P(A) + P(~A) = 1 => P(~A) = 1 - P(A)`

> Probabilidad Condicional: `P(A/B) = P(A ^ B) / P(B)` # Regla de Bayes

```
1.   P(A v B) = P(A) + P(B)
 ej: P(2 v 5) = P(2) + P(5) = 1/6 + 1/6 = 2/6 = 0.33 # Dados

2.   P(A v B) = P(A) + P(B) - P(A ^ B)      # P(A ^ B) -> Probabilidad Conjunta
 ej: P(5 v E) = P(5) + P(E) - P(5 ^ E) = 4/40 + 10/40 - 1/40 = 0.325 # Mazo de 40 cartas espaniolas

3.   P(A ^ B) = P(A) * P(B)
 ej: P(1 ^ 1) = P(1) * P(1) = 1/6 * 1/6 = 0.083
 ej: P(Blanca ^ Blanca) = P(Blanca) * P(Blanca) = 6/10 * 6/10 = 0.36 # Con reposicion 6B/4N
 ej: 1. Cual es la probabilidad de que la primera sea blanca y la 2da negra? P(B ^ N) = P(B) * P(N) = 6/10 * 4/10 = 0.24
     2. Cual es la probabilidad de que sean de distinto color? P((B ^ N) v (N ^ B)) = 2*(P(B) * P(N)) = 2 * (6/10 * 4/10) = 0.48
     3. Cual es la probabilidad de que al menos una sea blanca? P(al menos una blanca) = 1 - P(N ^ N) = 1 - (4/10 * 4/10) = 0.84
4.   P(A ^ B) = P(A) * P(B/A) # La probabilidad de que ocurra B si ya ocurrio A
 ej: P(B1 ^ B2) = P(B1) * P(B2/B1) = 6/10 * 5/9 = 0.33 # Sin reposicion 6B/4N
```

## Probabilidad Condicional

```
 P(A/B) = P(A ^ B) / P(B) ---> No Excluyentes => P(B) = P(A v B)
                          \
                           \-> Excluyentes Ai => Bayes (Teoria de la Probabilidad Total)
                                    Sum(P(Ai)) = 1 (Sistema Exhaustivo)
                                      P(B) = P(A1 ^ B) v P(A2 ^ B) v ...
                                      **  => P(B) = Sum(P(Ai) * P(B/Ai))

                        Bayes  ==> P(Ak/D) = P(Ak ^ D)  =   P(Ak) * P(D/Ak)
                                             ---------    --------------------
                                                P(D)      Sum(P(Ai) * P(D/Ai))
```

