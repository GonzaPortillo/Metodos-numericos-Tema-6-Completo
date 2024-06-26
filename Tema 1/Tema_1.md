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

       Resultado: El error relativo del 8% indica que la medición de la mesa
       tiene una discrepancia del 8% con respecto a su longitud real de 3 metros.

2. Un cirujano realiza una incisión en un procedimiento quirúrgico y la longitud objetivo de la incisión es de 10 centímetros. Sin embargo, al medir la incisión después del procedimiento, se encontró que mide 10.5 centímetros. Calcula el error relativo.

       Ea = | valor real - valor aproximado |
       Ea = | 10 - 10.5 | = | -0.5 | = 0.5 cm
   
       Er = Ea / Vr * 100
       Er = 0.5 /10 * 100 = 5%
   
       Resultado: El error relativo en la longitud de la incisión realizada por el cirujano es del 5%.
       Esto significa que la incisión es un 5% más larga de lo esperado.

## Error de Truncamiento
1. Estás en una tienda y ves un producto que cuesta $7.8912. Sin embargo, para hacer el cálculo mental más fácil, decides truncar el precio a la centésima, es decir, a $7.89. ¿Cuál es el error de truncamiento en esta situación?

##### *_Solucion_*

En este caso, el valor verdadero es $7.8912, pero la aproximación que hiciste fue de $7.89 (truncaste la parte decimal después de la centésima).

-El error verdadero (Ev) es la diferencia entre el valor verdadero y el valor aproximado:

        Ev = Valor verdadero − aproximado = 7. 8912 − 7. 89 = 0. 0012
● El error absoluto (|Ev|) es el valor absoluto de la diferencia entre del valor verdadero y la aproximación:
        
        |Ev| = |0. 0012| = 0. 0012
● El error relativo porcentual (εv) es el error verdadero dividido por el valor verdadero, expresado como porcentaje:

        εv = ( (Valor verdadero − aproximado) / Valor verdadero ) * 100% 
        εv = ( (7.8912 − 7.89) / 7.8912) * 100%
        εv = 0. 0152%

##### *_Justificación del resultado:_* 
Al truncar el precio de $7.8912 a $7.89, se incurre en un error verdadero de $0.0012, un error absoluto de $0.0012, y un error relativo porcentual de aproximadamente 0.0152%. Esto significa que pagaste un 0.0152% menos de lo que el producto realmente costaba.

2. Estás midiendo la longitud de un objeto con una regla que sólo tiene marcas para cada centímetro. Mides un objeto y determinas que tiene una longitud de 5.7 cm. Sin embargo, debido a las limitaciones de tu regla, sólo puedes informar la longitud como 5 cm. ¿Cuál es el error de truncamiento en esta situación?
   
##### *_Solución_* 
En este caso, el valor verdadero es 5.7 cm, pero la aproximación que hiciste fue de 5 cm (truncaste la parte decimal).

● El error verdadero (Ev) es la diferencia entre el valor verdadero y el valor aproximado:

        Ev = Valor verdadero − aproximado = 5. 7 − 5 = 0. 7
● El error absoluto (|Ev|) es el valor absoluto de la diferencia entre del valor verdadero y la aproximación:

        |Ev| = |0. 7| = 0. 7
● El error relativo porcentual (εv) es el error verdadero dividido por el valor verdadero, expresado como porcentaje:

        εv = ( (Valor verdadero − aproximado) /Valor verdadero) * 100%
        εv = ( (5.7 − 5) / 5.7) * 100%
        εv = 12.28%
        
##### *_Justificación del resultado:_*
Al truncar la longitud de 5.7 cm a 5 cm, se incurre en un error verdadero de 0.7 cm, un error absoluto de 0.7 cm, y un error relativo porcentual de aproximadamente 12.28%. Esto significa que la longitud que informaste es un 12.28% más corta que la longitud real del objeto.

## Error Absoluto
1. Se ha medido con una regla que tiene precisión de milímetros un lapicero, y el resultado de la medición ha sido 145,37 mm. La longitud exacta del lapicero es de 145 mm. ¿Qué error absoluto hemos cometido?

##### *_Solución_* 
    EA = Valor aproximado - Valor verdadero
    EA = 145,37 mm - 145 mm
    EA = 0,37 mm

2. Una persona, cuya masa real es de 63,874 kg, ha ido a la báscula de la farmacia a pesarse, y el resultado ha sido de 64,2 kg. ¿Qué error absoluto se ha cometido?

##### *_Solución_* 
    EA = Valor aproximado - Valor verdadero
    EA = 64,2 kg - 63,874 kg
    EA = 0,326 kg

## Cifra sigficativa
1. ¿Cuáles son las cifras significativas de cada una de las siguientes cantidades?.

        5.37 Cs = 3
        35.000 Cs = 2
        0.0038 Cs = 2

Las cifras significativas siempre serán cualquier número diferente de cero, los ceros son significativos sólo cuando se encuentren entre dos dígitos.

2. Realizar las operaciones, teniendo en cuenta las reglas de redondeo.

        2.1. 5.15 + 10.000 + 12.6 + 128.1282

          5.15
         10.000
         12.6
        128.1282
        _________________
        155.8789 = 155.9


        2.2. 27.4 * 2 = 54.8


## Conclusiones
Existen diferentes tipos de errores y es importante saber cuales son y cómo identificarlos, al momento de realizar mediciones o cálculos nos ayuda saber el nivel de error que puede llegar a existir y compararlo con datos anteriores o que ya se conocían.

## Bibliografia
Seno de Alpha. (2021). Soluciones Error absoluto y Error relativo 3o ESO www.senodealpha.com. Seno de Alpha. Retrieved February 8, 2024, from
https://www.senodealpha.com/wp-content/uploads/2021/09/Soluciones-Ejercicios-Error-absoluto-Error-relativo-3ESO.pdf

Dr. Alejandro S. M. Santa Cruz. (2021, Mayo 18). Errores de Redondeo y de Truncamiento. Diapositiva 1. Retrieved February 8, 2024, from
https://www.modeladoeningenieria.edu.ar/images/MatSup/2020/Errores_de_Redondeo_y_Truncamiento_Parte_I.pdf

unProfesor. (2016, April 12). Qué es el error absoluto y el error relativo [Video]. YouTube.
https://www.youtube.com/watch?v=l69yxD718Jo
