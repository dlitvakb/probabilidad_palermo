## Tarea

1. Comprobar si la suma 7 es la situacion mas ventajosa para el jugador? en Dados, con el tiro de 2 dados
2. Tengo dinero para jugar 5 jugadas de ruleta, cual plan me da mayor posibilidad de ganar?
3. Tengo $100, hay una rifa mensual de $10 el numero, cual es la mejor estrategia? 10 pesos por mes o 100 pesos de una
4. En una maternidad anotan el Sexo de cada bebe que nace, cual de las siguientes alternativas es la mas probable?

> Jugadas para Desafio 2
> a. R,R,R,R,R
> b. R,N,R,N,R
> c. R,R,N,N,N

> Alternativas para Desafio 4
> a. En 10 nacimientos, 7 nenas
> b. En 100 nacimientos, 70 nenas

### Respuestas

```
1. P(7) = 2 * P(1 ^ 6) v 2 * P(2 ^ 5) v 2 * P(3 ^ 4) = 2 * (1/36) * 3 = 1/6

2.a P(R ^ R ^ R ^ R ^ R) = P(R) ** 5 = (18/37) ** 5 = 0.2725
2.b, c todas dan lo mismo

3. Depende cuantos numeros haya

4. La A, dado que en caso de equiprobabilidad, la ley de los grandes numeros dice que a mayor muestra, la frecuencia muestral tiende al 50%
```

## Ejercicio

> En el departamento de deportes de la UP se ofrece entrenamiento en Futbol y Basquet. El 15% de los estudiantes
> se anotan en Futbol, el 8% en Basquet y el 3% en ambos deportes.
> a) Cual es la probabilidad de que un nuevo alumno de la UP se anote en algun deporte?
> b) Si un nuevo alumno se anota en deporte, cual es la probabilidad de que lo haga en Basquet?

```
        | Basquet            |
 Futbol | Si       | No      | Total
 ---------------------------------------
 Si     | 0.03     | 0.12    | 0.15
 No     | 0.05     | 0.80    | 0.85
 ---------------------------------------
 Total  | 0.08     | 0.92    | 1

 a) P(deporte) = P(B v F) = P(B) + P(F) - P(B ^ F) = 0.08 + 0.15 - 0.03 = 0.20
 b) P(B/deporte) = P(B ^ deporte) / P(deporte) = P(B) * P(deporte/B) / P(deporte) = 0.08 * 1 / 0.20 = 0.4
```


