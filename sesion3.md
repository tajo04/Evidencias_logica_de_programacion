<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 


<!-- Su documentación aquí -->

# Actividad 3: Ejercicios de operaciones básicas en Java.

1. Suma y multiplicación: Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.

2. Resta y división: Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.

3. Operaciones combinadas: Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.

4. Operaciones con decimales: Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.

5. Incremento y decremento: Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.

6. Operador de asignación compuesta: Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.

7. Operadores lógicos: Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.

8. Operador ternario: Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.

# Solucion:

1. 

```java

import java.util.Scanner;

public class Ac1 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el primer número entero: ");
        int num1 = scanner.nextInt();

        System.out.print("Ingrese el segundo número entero: ");
        int num2 = scanner.nextInt();

        int suma = num1 + num2;
        int multiplicacion = num1 * num2;

        System.out.println("La suma de los números es: " + suma);
        System.out.println("La multiplicación de los números es: " + multiplicacion);

        scanner.close();
    }
}
```
2. 

```java

import java.util.Scanner;

public class Ac2 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el primer número entero: ");
        int num1 = scanner.nextInt();

        System.out.print("Ingrese el segundo número entero: ");
        int num2 = scanner.nextInt();

        int resta = num1 - num2;

        if (num2 != 0) {
            double division = (double) num1 / num2;
            
            System.out.println("La resta de los números es: " + resta);
            System.out.println("La división de los números es: " + division);
        } else {
            System.out.println("No es posible dividir por cero.");
        }

        scanner.close();
    }
}
```

3. 

```java

import java.util.Scanner;

public class Ac3 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el primer número entero: ");
        int num1 = scanner.nextInt();

        System.out.print("Ingrese el segundo número entero: ");
        int num2 = scanner.nextInt();

        System.out.print("Ingrese el tercer número entero: ");
        int num3 = scanner.nextInt();

        int suma = num1 + num2 + num3;
        int multiplicacion = num1 * num2;
        
        if (num3 != 0) {
            double division = (double) multiplicacion / num3;

            System.out.println("La suma de los tres números es: " + suma);
            System.out.println("La multiplicación del primer número por el segundo es: " + multiplicacion);
            System.out.println("La división del resultado entre el tercer número es: " + division);
        } else {
            System.out.println("No es posible dividir por cero.");
        }

        scanner.close();
    }
}

```

4. 

```java

import java.util.Scanner;

public class Ac4 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el primer número decimal: ");
        double num1 = scanner.nextDouble();

        System.out.print("Ingrese el segundo número decimal: ");
        double num2 = scanner.nextDouble();

        double suma = num1 + num2;
        double resta = num1 - num2;
        double multiplicacion = num1 * num2;

        if (num2 != 0) {
            double division = num1 / num2;

            System.out.println("La suma de los números es: " + suma);
            System.out.println("La resta de los números es: " + resta);
            System.out.println("La multiplicación de los números es: " + multiplicacion);
            System.out.println("La división de los números es: " + division);
        } else {
            System.out.println("No es posible dividir por cero.");
        }

        scanner.close();
    }
}
```

5. 

```java

public class Ac5 {
    public static void main(String[] args) {

        int numero = 10;
        numero++;
        System.out.println("Después de incrementar, el valor es: " + numero);

        numero--;
        System.out.println("Después de decrementar, el valor es: " + numero);
    }
}
```

6. 

```java

public class Ac6 {
    public static void main(String[] args) {

        int numero = 10;

        numero += 5;

        System.out.println("Después de sumar 5, el valor es: " + numero);
    }
}
```

7. 

```java

import java.util.Scanner;

public class Ac7 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el primer valor booleano (true/false): ");
        boolean valor1 = scanner.nextBoolean();

        System.out.print("Ingrese el segundo valor booleano (true/false): ");
        boolean valor2 = scanner.nextBoolean();

        boolean resultadoAND = valor1 && valor2;
        boolean resultadoOR = valor1 || valor2;
        boolean resultadoNOT1 = !valor1;
        boolean resultadoNOT2 = !valor2;

        System.out.println("Resultado de la operación AND: " + resultadoAND);
        System.out.println("Resultado de la operación OR: " + resultadoOR);
        System.out.println("Resultado de la operación NOT para el primer valor: " + resultadoNOT1);
        System.out.println("Resultado de la operación NOT para el segundo valor: " + resultadoNOT2);

        scanner.close();
    }
}
```

8. 

```java

import java.util.Scanner;

public class Ac8 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese un número entero: ");
        int numero = scanner.nextInt();

        String resultado = (numero >= 0) ? "positivo" : "negativo";

        System.out.println("El número ingresado es " + resultado);

        scanner.close();
    }
}
```