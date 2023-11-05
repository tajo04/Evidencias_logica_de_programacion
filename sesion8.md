<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->
# Actividad: Ejecicios de métodos en Java
## Implementar los siguientes métodos:

1. Escribe un método que reciba dos números como parámetros y evuelva el mayor de los dos.
2. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
3. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
4. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
5. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

## Solucion:

1. 

```java

public class Ac1 {

    public static void main(String[] args) {

        int numero1 = 15;
        int numero2 = 7;

        int resultado = obtenerMayor(numero1, numero2);

        System.out.println("El número mayor es: " + resultado);
    }


    public static int obtenerMayor(int num1, int num2) {
        return (num1 > num2) ? num1 : num2;
    }
}

```
2. 

```java

public class Ac2 {

    public static void main(String[] args) {

        String texto = "Hola, ¿cómo estás?";

        int cantidadVocales = contarVocales(texto);

        System.out.println("El número de vocales en el texto es: " + cantidadVocales);
    }

    public static int contarVocales(String texto) {
        int contadorVocales = 0;

        for (char letra : texto.toLowerCase().toCharArray()) {
            if (esVocal(letra)) {
                contadorVocales++;
            }
        }

        return contadorVocales;
    }

    private static boolean esVocal(char letra) {
        return "aeiou".indexOf(letra) != -1;
    }
}

```
3. 

```java

public class Ac3 {

    public static void main(String[] args) {

        String texto = "Hola, MUndo!";

        String resultado = invertirMayusculasMinisculas(texto);

        System.out.println("Resultado: " + resultado);
    }


    public static String invertirMayusculasMinisculas(String texto) {
        StringBuilder resultado = new StringBuilder();

        for (char letra : texto.toCharArray()) {
            if (Character.isUpperCase(letra)) {
                resultado.append(Character.toLowerCase(letra));
            } else if (Character.isLowerCase(letra)) {
                resultado.append(Character.toUpperCase(letra));
            } else {
                resultado.append(letra);
            }
        }

        return resultado.toString();
    }
}

```

4. 

```java

public class Ac4 {

    public static void main(String[] args) {

        String texto = "Este es un ejemplo de conteo de palabras.";

        int cantidadPalabras = contarPalabras(texto);

        System.out.println("El número de palabras en el texto es: " + cantidadPalabras);
    }


    public static int contarPalabras(String texto) {

        texto = texto.trim();


        if (texto.isEmpty()) {
            return 0;
        }


        String[] palabras = texto.split("\\s+");


        return palabras.length;
    }
}

```

5. 

```java

import java.util.Arrays;

public class Ac5 {

    public static void main(String[] args) {

        String texto = "Java es un lenguaje de programación";

        String resultado = ordenarPalabrasAlfabeticamente(texto);

        System.out.println("Palabras ordenadas alfabéticamente: " + resultado);
    }


    public static String ordenarPalabrasAlfabeticamente(String texto) {

        String[] palabras = texto.split(" ");


        Arrays.sort(palabras);


        return String.join(" ", palabras);
    }
}

```

