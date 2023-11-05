<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


<!-- Su documentación aquí -->

# Actividad: Ejecicios Array - ArrayList

1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

### Ejemplo Array

```java

import java.util.Arrays;

public class EjercicioArray {

    public static void main(String[] args) {
        // Crear un array de números enteros
        int[] numeros = {5, 2, 10, 7, 1};

        // Imprimir el array original
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Calcular la suma de los elementos del array
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
    }
}
```
### Ejemplo Array list

```java

import java.util.ArrayList; 
import java.util.Scanner;

public class AppNotas {

  public static void main(String[] args) {

    ArrayList<String> notas = new ArrayList<>();
    
    Scanner scan = new Scanner(System.in);

    while(true) {

      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      int opcion = scan.nextInt();

      if (opcion == 1) {
        agregarNota(notas, scan);  
      } else if (opcion == 2) {
        mostrarNotas(notas);
      } else {
        break;
      }

    }

  }

  public static void agregarNota(ArrayList<String> notas, Scanner scan) {
    
    System.out.println("Ingrese el titulo de la nota:");
    String titulo = scan.nextLine();
    
    System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();
    
    notas.add(titulo + " - " + contenido);

  }

  public static void mostrarNotas(ArrayList<String> notas) {

    for(String n : notas) {
      System.out.println(n);
    }

  }

}
```

2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.

## Solucion:

### 1. Array

1. Se crea un array llamado numeros con los valores {5, 2, 10, 7, 1}.

2. Se imprime el array original.

3. Se calcula la suma de los elementos del array.

4. Se encuentra el número más grande en el array.

5. Se ordena el array en orden ascendente utilizando Arrays.sort().

* La salida esperada muestra el array original, la suma de sus elementos, el número más grande y el array ordenado. El código ilustra el uso básico de arrays en Java y cómo realizar operaciones comunes como suma, búsqueda y ordenamiento.

### 2. Array list

```java

import java.util.ArrayList;
import java.util.Scanner;

public class AppNotas {

  public static void main(String[] args) {

    // Crear un ArrayList para almacenar las notas
    ArrayList<String> notas = new ArrayList<>();
    
    // Crear un objeto Scanner para la entrada del usuario
    Scanner scan = new Scanner(System.in);

    // Menú de opciones en un bucle while
    while (true) {

      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      // Leer la opción del usuario
      int opcion = scan.nextInt();

      // Realizar acciones según la opción seleccionada
      if (opcion == 1) {
        agregarNota(notas, scan);  
      } else if (opcion == 2) {
        mostrarNotas(notas);
      } else {
        break;
      }

    }

  }

  // Método para agregar una nueva nota al ArrayList
  public static void agregarNota(ArrayList<String> notas, Scanner scan) {
    
    // Solicitar al usuario que ingrese el título de la nota
    System.out.println("Ingrese el título de la nota:");
    // Consumir el carácter de nueva línea pendiente
    scan.nextLine();
    String titulo = scan.nextLine();
    
    // Solicitar al usuario que ingrese el contenido de la nota
    System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();
    
    // Agregar la nota al ArrayList
    notas.add(titulo + " - " + contenido);

  }

  // Método para mostrar todas las notas en el ArrayList
  public static void mostrarNotas(ArrayList<String> notas) {

    // Iterar sobre el ArrayList y mostrar cada nota
    for (String n : notas) {
      System.out.println(n);
    }

  }

}
```

* El programa permite gestionar un conjunto de notas interactuando con el usuario.
* Se utiliza un bucle while para mostrar un menú de opciones.
* Las opciones incluyen agregar notas, mostrar todas las notas o salir del programa.
* Los métodos agregarNota y mostrarNotas facilitan la interacción con el ArrayList de notas.
* El programa utiliza un objeto Scanner para la entrada del usuario y un ArrayList para almacenar las notas de manera dinámica.


## Ejemplos

### Array

```java

import java.util.Arrays;

public class Array {
    public static void main(String[] args) {

        double[] distancias = {10.5, 5.2, 8.7, 12.0, 6.8};


        for (double distancia : distancias) {

        }
    }
}
```
### Array list

```java

import java.util.ArrayList;

public class ArrayList {
    public static void main(String[] args) {

        ArrayList<String> ciudades = new ArrayList<>();


        ciudades.add("París");
        ciudades.add("Nueva York");
        ciudades.add("Tokio");


        for (String ciudad : ciudades) {

        }
    }
}
```






