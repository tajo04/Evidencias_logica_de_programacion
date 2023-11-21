<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->

## Actividad: Prueba, ejecución y explicación de ejercicios de lógica de programación.

1. Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno.

```java 

import java.util.Scanner;
import java.text.DecimalFormat;

public class Main {
    public static void main(String[] args) {
        // Crear un objeto DecimalFormat para formatear la salida
        DecimalFormat decimalFormat = new DecimalFormat("#,###");

        // Crear un objeto Scanner para la entrada del usuario
        Scanner scanner = new Scanner(System.in);

        // Saludar al usuario
        System.out.println("Bienvenido al calculador de CDT!");

        // Pedir al usuario que ingrese los datos del CDT
        System.out.print("Ingrese el monto del depósito: ");
        double montoDeposito = scanner.nextDouble();

        System.out.print("Ingrese la tasa de interés anual (%): ");
        double tasaInteresAnual = scanner.nextDouble();

        System.out.print("Ingrese el plazo en meses: ");
        int plazoMeses = scanner.nextInt();

        // Calcular el interés y el monto total al vencimiento
        double tasaInteresMensual = tasaInteresAnual / 12 / 100;
        double interesMensual = montoDeposito * tasaInteresMensual;
        double montoTotalVencimiento = montoDeposito + (interesMensual * plazoMeses);

        // Mostrar el resumen del CDT
        System.out.println("Resumen del CDT:");
        System.out.println("- Monto del depósito: $" + decimalFormat.format(montoDeposito));
        System.out.println("- Tasa de interés anual: " + tasaInteresAnual + "%");
        System.out.println("- Plazo en meses: " + plazoMeses);
        System.out.println("- Interés mensual: $" + decimalFormat.format(interesMensual));
        System.out.println("- Monto total al vencimiento: $" + decimalFormat.format(montoTotalVencimiento));
    }
}
```

### Explicación:

#### Importaciones:

Se importan las clases Scanner y DecimalFormat para facilitar la entrada de datos y formatear la salida, respectivamente.

#### Inicialización de objetos:

 * Se crea un objeto DecimalFormat para formatear los valores monetarios.
Se crea un objeto Scanner para la entrada del usuario.

#### Entrada de datos:

 * Se solicita al usuario que ingrese el monto del depósito, la tasa de interés anual y el plazo en meses.

#### Cálculos:

 * Se calcula la tasa de interés mensual.
 * Se calcula el interés mensual y el monto total al vencimiento.

#### Salida de resultados:

 * Se muestra un resumen detallado del CDT, incluyendo el monto del depósito, la tasa de interés, el plazo, el interés mensual y el monto total al vencimiento.

2. Calcular la cantidad de materiales necesarios para construir una pared de ladrillos

```java

import java.util.Scanner;

public class CantidadLadrillos {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double largo, alto, ancho, areaPared, cantidadLadrillos, largoLadrillo, altoLadrillo, anchoLadrillo;
      
      // Solicita las dimensiones de la pared
      System.out.print("Ingrese el largo de la pared en metros: ");
      largo = input.nextDouble();
      System.out.print("Ingrese el alto de la pared en metros: ");
      alto = input.nextDouble();
      System.out.print("Ingrese el ancho de la pared en metros: ");
      ancho = input.nextDouble();

      // Solicita las dimensiones del ladrillo
      System.out.print("Ingrese el largo del ladrillo en metros: ");
      largoLadrillo = input.nextDouble();
      System.out.print("Ingrese el alto del ladrillo en metros: ");
      altoLadrillo = input.nextDouble();
      System.out.print("Ingrese el ancho del ladrillo en metros: ");
      anchoLadrillo = input.nextDouble();

      // Calcula el área de la pared y del ladrillo
      areaPared = largo * alto;
      double areaLadrillo = largoLadrillo * altoLadrillo;

      // Calcula la cantidad de ladrillos necesarios
      cantidadLadrillos = Math.ceil(areaPared / (areaLadrillo * ancho / anchoLadrillo));

      // Muestra el resultado en la consola
      System.out.printf("Para construir la pared se necesitan %.0f ladrillos.", cantidadLadrillos);
   }
}

```

### Eplicacion:

1) #### Importamos la clase Scanner: 
   + Esto nos permite leer la entrada del usuario.
2) #### Declaramos las variables:
   + Largo, alto y ancho de la pared, así como las dimensiones del ladrillo, área de la pared, cantidad de ladrillos y dimensiones del área del ladrillo.
3) #### Solicitamos al usuario que ingrese las dimensiones:
   +  Utilizamos System.out.print para mostrar mensajes y input.nextDouble() para obtener datos del usuario.
4) #### Calculamos el área de la pared y del ladrillo:
   + Usamos las fórmulas areaPared = largo * alto y areaLadrillo = largoLadrillo * altoLadrillo.
5) #### Calculamos la cantidad de ladrillos necesarios:
   + Utilizamos la fórmula (areaPared / (areaLadrillo * ancho / anchoLadrillo)) y aplicamos Math.ceil() para redondear hacia arriba, ya que no se pueden tener fracciones de ladrillos.
6) #### Mostramos el resultado en la consola:
   + Utilizamos System.out.printf para formatear y mostrar el resultado.