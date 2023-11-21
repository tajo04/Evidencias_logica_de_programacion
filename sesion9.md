<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 

### Ejercicios de Lógica de Programación
 Calculadora de resistencias eléctricas

1. Resolver en parejas el ejercicio asignado por el docente

```java

import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

 

class Main {
  public static void main(String[] args) {
   
        Map<String, Integer> colores = new HashMap<>();
        colores.put("negro", 0);
        colores.put("marron", 1);
        colores.put("rojo", 2);
        colores.put("naranja", 3);
        colores.put("amarillo", 4);
        colores.put("verde", 5);
        colores.put("azul", 6);
        colores.put("violeta", 7);
        colores.put("gris", 8);
        colores.put("blanco", 9);

        Scanner scanner = new Scanner(System.in);
        String[] bandas = new String[3];

        for (int i = 0; i < 3; i++) {
            System.out.print("Introduce el color de la banda " + (i + 1) + ": ");
            bandas[i] = scanner.nextLine().toLowerCase();
            if (!colores.containsKey(bandas[i])) {
                System.out.println("Color no válido. Introduce un color válido.");
                i--; // Repetir la entrada si el color no es válido
            }
        }

        int valor = (colores.get(bandas[0]) * 10 + colores.get(bandas[1])) * (int) Math.pow(10, colores.get(bandas[2]));
    

        System.out.println("El valor de la resistencia es: " + valor / 1000 + "k ohmios");
    }
}
```




