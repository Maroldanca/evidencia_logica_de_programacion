<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 

## Actividad: Ejecicios Array - ArrayList
1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

Ejemplo Array

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

Ejemplo Array list

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

### Solucion

**Arrays**
```java
public static void main(String[] args) {
        
        int[] numerosPares = {2,4,6,8,10,12,14};
        
        System.out.println("El array original es: " + Arrays.toString(numerosPares));
        
         int suma = 0;
        for (int i = 0; i < numerosPares.length; i++) {
            suma += numerosPares[i];
        }
        System.out.println("La suma de los elementos es: " + suma);
        
        int maximo = numerosPares[0];
        for (int i = 1; i < numerosPares.length; i++) {
            if (numerosPares[i] > maximo) {
                maximo = numerosPares[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);
```

**ArrayList**

```java
import java.util.Arrays;
import java.util.ArrayList;
import java.util.Scanner;

/**
 *
 * @author Miguel Angel
 */
public class Pruebas {

    public static void main(String[] args) {

        ArrayList<String> vehiculos = new ArrayList<>();
        Scanner sc = new Scanner(System.in);

       while(true){

            System.out.println("1. Agregar carro");
            System.out.println("2. Mostrar carros");
            System.out.println("3. Salir");

            int opcion = sc.nextInt();

            if (opcion == 1) {
                añadirCarro(vehiculos, sc);
            } else if (opcion == 2) {
                listaCarros(vehiculos);
            } else {
                break;
                
            }
       }
        
    }

    public static void añadirCarro(ArrayList<String> vehiculos, Scanner sc) {
        System.out.println("Ingresa tu nuevo carro");

        String nuevoCarro = sc.nextLine();

        vehiculos.add(nuevoCarro);

    }

    public static void listaCarros(ArrayList<String> vehiculos) {

        for (String carros : vehiculos) {
            System.out.println(carros);
        }
    }
}
```






