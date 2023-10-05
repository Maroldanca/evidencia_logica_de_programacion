<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


## Actividad: Ejecicios de métodos en Java
Implementar los siguientes métodos:

- Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

### Solucion

### Escribe un metodo que reciba dos numeros como parametros y devuelva el mayor de los 2

``` java
public class MayorDeDosNumeros {
    public static void main(String[] args) {
        int numero1 = 10;
        int numero2 = 20;
        int mayor = mayorNumero(numero1, numero2);
        System.out.println("El número mayor es: " + mayor);
    }

    public static int mayorNumero(int numero1, int numero2) {
        if (numero1 > numero2) {
            return numero1;
        } else {
            return numero2;
        }
    }
}
```

### Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.

``` java
public class ContarVocales {
    public static void main(String[] args) {
        String texto = "Hola, ¿cómo estás?";
        int cantidadVocales = contarVocales(texto);
        System.out.println("El número de vocales en el texto es: " + cantidadVocales);
    }

    public static int contarVocales(String texto) {
        int contadorVocales = 0;

        texto = texto.toLowerCase();

        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u') {
                contadorVocales++;
            }
        }

        return contadorVocales;
    }
}
```

### Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa

``` java
public class CambiarMayusculasMinisculas {
    public static void main(String[] args) {
        String texto = "Hola Mundo";
        String resultado = cambiarMayusculasMinisculas(texto);
        System.out.println("Texto modificado: " + resultado);
    }

    public static String cambiarMayusculasMinisculas(String texto) {
        char[] caracteres = texto.toCharArray();

        for (int i = 0; i < caracteres.length; i++) {
            char caracter = caracteres[i];
            if (Character.isUpperCase(caracter)) {
                caracteres[i] = Character.toLowerCase(caracter);
            } else if (Character.isLowerCase(caracter)) {
                caracteres[i] = Character.toUpperCase(caracter);
            }
        }

        return new String(caracteres);
    }
}
```

### Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene

``` java
public class ContarPalabras {
    public static void main(String[] args) {
        String texto = "Buenos dias grupo como han estado el dia de hoy";

        int cantidadPalabras = contarPalabras(texto);
        System.out.println("El número de palabras en el texto es: " + cantidadPalabras);
    }

    public static int contarPalabras(String texto) {
        String[] palabras = texto.split("\\s+"); 
        return palabras.length;
    }
}
```

### Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.
``` java
import java.util.Arrays;

public class OrdenarPalabras {
    public static void main(String[] args) {
        String texto = "Funcionando esta cadena de texto en varias palabras.";
        String resultado = ordenarPalabras(texto);
        System.out.println("Palabras ordenadas: " + resultado);
    }

    public static String ordenarPalabras(String texto) {
        
        String[] palabras = texto.split("\\s+");

       
        Arrays.sort(palabras);

        String resultado = String.join(" ", palabras);

        return resultado;
    }
}
```




