# Ejercicios

```
1. Un banco ofrece 2 productos, apertura de cuenta corriente y tarjeta de credito,
   con costos de mantenimiento de 20 y 15 pesos mensuales respectivamente. De
   acuerdo a promociones anteriores, estiman que el 38% de clientes potenciales
   aceptan la cuenta corriente, el 55% aceptan la tarjeta y el 30% ambos productos.

a. Construir la distribucion de probabilidad del gasto de mantenimiento
   mensual por cliente
b. Cual es la probabilidad de que un cliente haga un pago por mantenimiento
c. Cual es el gasto esperado y el mantenimiento por cliente y su desvio
d. Cuanto esperaria cobrar el banco si contacta a
   2000 potenciales clientes y el desvio
```


```
         | Cuenta Corriente |
 Tarjeta | Si     | No      | Total
 -----------------------------------
 Si      | 0.3    | 0.25    | 0.55
 No      | 0.08   | 0.37    | 0.45
 -----------------------------------
 Total   | 0.38   | 0.62    |     1

a)
 Mantenimiento | P
 35            | 0.3
 20            | 0.08
 15            | 0.25
 0             | 0.37

b) P(Mant) = P(CC v T) = P(CC) + P(T) - P(CC ^ T) = 0.38 + 0.55 - 0.3 = 0.63

c) E(Mant) = 35 * P(35) + 20 * P(20) + 15 * P(15) = 15.85

   σ**2(Mant) = ((35 - 15.85)**2 * 0.3) + ((20 - 15.85)**2 * 0.08) +
                ((15 - 15.85)**2 * 0.25) + ((0 - 15.85)**2 * 0.37) = 204.5275
   σ(Mant) = 14.30

d) W = Ingreso Mensual
   E(2000W) = 2000 * E(Mant) = 31700
   σ(2000W) = Sqrt(2000 * σ**2(Mant)) = 639.57
```

Hacer 17, 18 y 25 de guia ejercicios

```
Dos amigos A y B practican tiro al blanco, con una efectividad del 90 y 80%
respectivamente. Ayer uno de ellos hizo una practica de 8 disparos y obtuvo
6 aciertos.

Cual es la probabilidad de que le haya ocurrido a A?

     P(acierto) = 0.9
     X = nro de aciertos en set de 8 disparos
     PbiA(X=6/8;0.9) = 8C6 * 0.9**6 * 0.1**2 = 0.1488
     PbiB(X=6/8;0.8) = 8C6 * 0.8**6 * 0.2**2 = 0.2936
     P(A/6 ac en 8) = P(A) * P(6 en 8/A)
                     ---------------------
                     (P(A) * P(6 en 8/A) + P(B) * P(6 en 8/B))
                    = 0.5 * 0.1488
                     --------------
                     (0.5 * 0.1488 + 0.5 * 0.2936)
                    = 0.3363
```

