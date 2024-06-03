# Métodos de Solución de Ecuaciones

## Introduccion

Los métodos de solución de ecuaciones son técnicas utilizadas para encontrar los valores de las variables que satisfacen una ecuación dada. Dependiendo del tipo de ecuación, se pueden utilizar diferentes métodos.

Los metodos que veremos en esta ocacion son:

1. Biseccion: Es un método numérico utilizado para encontrar las raíces de una función continua. Consiste en dividir repetidamente un intervalo en dos partes y seleccionar el subintervalo en el que existe un cambio de signo de la función, lo que indica la presencia de una raíz. Este proceso se repite hasta que se alcanza un intervalo suficientemente pequeño, proporcionando una aproximación de la raíz.
2. Regla falsa: También conocido como método de interpolación lineal o método de la secante, es un método numérico para encontrar raíces de funciones continuas. A diferencia del método de bisección, que divide el intervalo por la mitad, la regla falsa utiliza una interpolación lineal entre los puntos finales del intervalo para estimar la raíz. Este método converge más rápidamente que el método de bisección en ciertos casos.
3. Secante: Es un método numérico para encontrar raíces de una función continua. Es similar al método de la regla falsa, pero en lugar de mantener un intervalo que contiene la raíz, utiliza dos aproximaciones sucesivas de la raíz para iterativamente acercarse a la solución. Este método generalmente converge más rápido que el método de bisección y la regla falsa.

## Algoritmos

### Biseccion

1. Definir la función ( f(x) ) y los extremos del intervalo ([a, b]) tal que ( f(a) \cdot f(b) < 0 ).
2. Calcular el punto medio ( c = \frac{a + b}{2} ).
3. Evaluar ( f(c) ). Si ( f(c) = 0 ) o el intervalo es suficientemente pequeño (criterio de convergencia), entonces ( c ) es la raíz. Si ( f(a) \cdot f(c) < 0 ), entonces la raíz está en el intervalo ([a, c]). De lo contrario, la raíz está en ([c, b]).
4. Repetir el proceso con el nuevo intervalo hasta que se cumpla el criterio de convergencia.

### Regla falsa 

1. Definir f(x).
2. Definir los intervalos [a,b].
3. Defiinr el umbral.
4. Calcular el punto de intersección 𝑐 de la línea que une (af(a) y (b,f(b)).
5. Evaluar f(c).
6. Repetir los pasos anteriores hasta que se cumpla la condición de parada.

### Secante

1. Definir f(x).
2. Definir dos aproximaciones iniciales X0 y X1.
3. Definir el umbral de tolerancia.
4. Para i=1 hasta maxIter.
5. Calcular Xi+1 usando la formula.
6. Retornar Xi+1 como la raíz aproximada si se ha alcanzado la tolerancia, o el valor más cercano después de maxIter iteraciones.

## Implementacion en Java

### Biseccion

    public class Biseccion {
    
      public static double funcion(double x) {
        return x * x * x - x - 2; //f(x) = x^3 - x - 2
      }

      public static double biseccion(double a, double b, double tolerancia, int maxIteraciones) {
        if (funcion(a) * funcion(b) >= 0) {
            System.out.println("El método de bisección no se puede aplicar.");
            return Double.NaN;
        }
        
        double c = a;
        for (int i = 0; i < maxIteraciones; i++) {
            c = (a + b) / 2;

            if (funcion(c) == 0.0 || (b - a) / 2 < tolerancia) {
                return c;
            }

            if (funcion(c) * funcion(a) < 0) {
                b = c;
            } else {
                a = c;
            }
        }
        
        return c;
      }

      public static void main(String[] args) {
        double a = 1; // Límite inferior del intervalo
        double b = 2; // Límite superior del intervalo
        double tolerancia = 1e-6; // Tolerancia
        int maxIteraciones = 1000; // Número máximo de iteraciones
        
        double raiz = biseccion(a, b, tolerancia, maxIteraciones);
        
        if (!Double.isNaN(raiz)) {
            System.out.printf("La raíz encontrada es: %.6f\n", raiz);
        } else {
            System.out.println("No se encontró una raíz en el intervalo dado.");
        }
      }
    }

### Regla falsa 

    public class ReglaFalsa {
    
        public static double funcion(double x) {
            return x * x - 4; // Ejemplo: f(x) = x^2 - 4
        }

        public static double reglaFalsa(double a, double b, double tol, int maxIter) {
            double fa = funcion(a);
            double fb = funcion(b);
        
            if (fa * fb > 0) {
                System.out.println("La función no cambia de signo en el intervalo dado.");
                return Double.NaN;
            }

            double c = a; // Inicialización de c

            for (int iter = 0; iter < maxIter; iter++) {
                // Calculamos el punto c usando la fórmula de la regla falsa
                c = b - fb * (b - a) / (fb - fa);
                double fc = funcion(c);
            
                // Comprobamos la tolerancia
                if (Math.abs(fc) < tol) {
                    System.out.println("La raíz encontrada es: " + c);
                    return c;
                }
            
                // Actualizamos los valores de a y b
                if (fa * fc < 0) {
                    b = c;
                    fb = fc;
                } else {
                    a = c;
                    fa = fc;
                }
            }
        
            System.out.println("No se encontró la raíz después de " + maxIter + " iteraciones.");
            return c;
        }

        public static void main(String[] args) {
            double a = 0; // Intervalo inferior
            double b = 3; // Intervalo superior
            double tol = 1e-6; // Tolerancia
            int maxIter = 100; // Número máximo de iteraciones

            double raiz = reglaFalsa(a, b, tol, maxIter);
            System.out.println("La raíz aproximada es: " + raiz);
        }
    }

### Secante

    public class Secante {

        // Definir la función de la que queremos encontrar la raíz
        public static double f(double x) {
            return x * x * x - x * x + 2; // Ejemplo de función: x^3 - x^2 + 2
        }

        // Implementación del método de la secante
        public static double secantMethod(double x0, double x1, double tol, int maxIter) {
            double f0 = f(x0);
            double f1 = f(x1);
            double x2 = 0.0;
            int iter = 0;

            while (Math.abs(f1) > tol && iter < maxIter) {
                x2 = x1 - f1 * ((x1 - x0) / (f1 - f0)); // Fórmula del método de la secante
                x0 = x1;
                f0 = f1;
                x1 = x2;
                f1 = f(x1);
                iter++;
            }

            if (iter >= maxIter) {
                System.out.println("El método no convergió en " + maxIter + " iteraciones.");
            }

            return x2;
        }

        public static void main(String[] args) {
            double x0 = -20; // Valor inicial 1
            double x1 = -10; // Valor inicial 2
            double tol = 1e-6; // Tolerancia
            int maxIter = 100; // Número máximo de iteraciones

            double root = secantMethod(x0, x1, tol, maxIter);
            System.out.println("La raíz encontrada es: " + root);
        }
    }
