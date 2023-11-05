<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


<!-- Su documentación aquí -->
# Actividad 5: Ejercicios de bucles
## Resolver los siguientes ejercicios:

### Ejercicios - while

1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.

2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.

### Ejercicios - do while

1. Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.

2. Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

### Ejercicios - for

1. Imprimir los números impares del 1 al 50.

2. Imprimir los números primos del 1 al 100.
   

## Solucion:

### Ejercicios - while
1. 

```java

import java.util.Scanner;

public class Cl5 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese un número para ver su tabla de multiplicar: ");
        int numero = scanner.nextInt();

        int contador = 1;
        while (contador <= 10) {
            System.out.println(numero + " x " + contador + " = " + (numero * contador));
            contador++;
        }

        scanner.close();
    }
}
```

2. 

```java

import java.util.Scanner;

public class Cl5 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese una cadena de caracteres: ");
        String cadena = scanner.nextLine();

        int contadorNumeros = 0;
        int i = 0;
        while (i < cadena.length()) {
            char caracter = cadena.charAt(i);
            if (Character.isDigit(caracter)) {
                contadorNumeros++;
            }
            i++;
        }

        System.out.println("La cantidad de caracteres que son números en la cadena es: " + contadorNumeros);

        scanner.close();
    }
}

```
### Ejercicios - do while

1. 

```java 

import java.util.Scanner;

public class Cl5 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int numero;
        do {
            System.out.print("Ingrese un número (ingrese un número negativo para detener): ");
            numero = scanner.nextInt();
        } while (numero >= 0);

        int i = 1;
        do {
            System.out.println(i);
            i++;
        } while (i <= 100);

        scanner.close();
    }
}
```

2. 

```java

import java.util.Scanner;

public class Cl5 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese un número para ver su tabla de multiplicar (ingrese 0 para detener): ");
        int numero = scanner.nextInt();

        do {
            int contador = 1;
            while (contador <= 10) {
                System.out.println(numero + " x " + contador + " = " + (numero * contador));
                contador++;
            }

            System.out.print("Ingrese otro número (ingrese 0 para detener): ");
            numero = scanner.nextInt();

        } while (numero != 0);

        scanner.close();
    }
}
```
### Ejercicios - for
1. 

```java

public class NumerosImpares {
    public static void main(String[] args) {
        System.out.println("Números impares del 1 al 50:");

        for (int i = 1; i <= 50; i += 2) {
            System.out.println(i);
        }
    }
}
```
2. 

```java

public class NumerosPrimosSinClases {
    public static void main(String[] args) {
        System.out.println("Números primos del 1 al 100:");

        for (int i = 2; i <= 100; i++) {
            if (esPrimo(i)) {
                System.out.println(i);
            }
        }
    }

    private static boolean esPrimo(int numero) {
        if (numero <= 1) {
            return false;
        }

        for (int i = 2; i <= Math.sqrt(numero); i++) {
            if (numero % i == 0) {
                return false;
            }
        }

        return true;
    }
}
```