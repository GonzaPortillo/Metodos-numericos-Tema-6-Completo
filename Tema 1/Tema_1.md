# Introduccion a Metodos Numericos

## Contenido

1. Error de redondeo
2. Error Relativo
3. Error de Truncamiento
4. Error Absoluto
5. Cifra Significativa
6. Conclusiones
7. Bibliografía

## Error de truncamiento 

1. Calcula el valor de la expresión 1⁄3 + 1⁄5 + 1/7 con cuatro cifras decimales y sin redondear ningún número intermedio. Luego, repite el cálculo redondeando cada fracción a dos cifras decimales antes de sumarlas. ¿Cuál es el error de redondeo absoluto y relativo que se produce al hacer esto?

        0.3333 + 0.2000 + 0.1428 = 0.6762

        Redondeo a dos cifras decimales
        0.33 + 0.20 + 0.14 = 0.67

2. Calcula el área de un círculo de radio 3.2 cm con cuatro cifras decimales y sin redondear ningún número intermedio. Luego, repite el cálculo redondeando el valor de π a dos cifras decimales antes de operar. ¿Cuál es el error de redondeo absoluto y relativo que se produce al hacer esto?

        A = π(3.2)^2
        A = 3.1416 x 10.24
        A = 32.1699 cm^2

        π redondeado a dos cifras decimales
         A = 3.14 (3.2)^2
         A = 3.14 x 10.24
         A = 32.1536 cm^2
         A = 32.15 cm^2

        Error de redondeo absoluto:
         32.1699 - 32.1536 = 0.0163
   
        Error de redondeo relativo:
         (0.0163/32.1699)*100 = 0.051%

## Error Relaivo

1. Se encuentra una mesa que mide 3m de largo, pero al medirla se obtiene un valor de 3.24m. ¿Cuál es su error relativo?

       Ea = | valor real - valor aproximado |
       Ea = | 3 - 3.24 | = | -0.24 | = 0.24 m
   
       Er = Ea / Vr * 100
       Er = 0.24 /3 * 100 = 8%

       Resultado: El error relativo del 8% indica que la medición de la mesa tiene una discrepancia del 8% con respecto a su longitud real de 3 metros.

2. Un cirujano realiza una incisión en un procedimiento quirúrgico y la longitud objetivo de la incisión es de 10 centímetros. Sin embargo, al medir la incisión después del procedimiento, se encontró que mide 10.5 centímetros. Calcula el error relativo.

       Ea = | valor real - valor aproximado |
       Ea = | 10 - 10.5 | = | -0.5 | = 0.5 cm
   
       Er = Ea / Vr * 100
       Er = 0.5 /10 * 100 = 5%
   
       Resultado: El error relativo en la longitud de la incisión realizada por el cirujano es del 5%. Esto significa que la incisión es un 5% más larga de lo
esperado.

## Error de Truncamiento

## Error Absoluto

## Conclusiones

## Bibliografia

