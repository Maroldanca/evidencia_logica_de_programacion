<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 

## Actividad: Ejercicios de Lógica de Programación

- Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

- Desarrollar un algoritmo que realice la conversión de binario a decimal.


### Solucion

1.
```java
public class Mavenproject1 {

    public static void main(String[] args) {
        // Declaramos un conjunto de números enteros
        int[] numeros = {1, 2, 3, 4, 5, 2};

        // Creamos una variable para almacenar el número que aparece más de una vez
        int numeroRepetido = 0;

        //añadios una lista de arreglo
        ArrayList<Integer> numerosRepetidos = new ArrayList<>();
        
        // Recorremos el conjunto de números
        for (int i = 0; i < numeros.length; i++) {
            // Comprobamos si el número actual ya ha aparecido
            for (int j = 0; j < i; j++) {
                if (numeros[i] == numeros[j]) {
                    // El número actual ya ha aparecido
                    numeroRepetido = numeros[i];
                    
                    //se revisa si existe otro numero
                    if (numeros[i] == numeros[j] && !numerosRepetidos.contains(numeros[i]));
                    
                    // se añade a la lista
                    numerosRepetidos.add(numeros[i]);
                    break;
                }
            }
        }

        // Si el número repetido es distinto de 0, lo imprimimos
        if (numeroRepetido != 0) {
            System.out.println("El/los numeros repetido/s son: " + numerosRepetidos);
        } else {
            // No hay ningún número repetido
            System.out.println("No hay ningún número repetido");
        }
    }
}
```

2.






