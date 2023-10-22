<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 
 
 ### Actividad: Ejercicios de Lógica de Programación
1- Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

2- Desarrollar un algoritmo que realice la conversión de binario a decimal.

### Solucion

1- 
```java
 *
 * @author Miguel Angel
 */
public class Pruebas {

    public static void main(String[] args) {
        
        int[] numeros = {1, 2, 3, 4, 5, 2, 3, 4, 6};

        ArrayList<Integer> numerosRepetidos = new ArrayList<>();


        for (int i = 0; i < numeros.length; i++) {
           
            for (int j = 0; j < i; j++) {
                if (numeros[i] == numeros[j]) {
                    
                    if (!numerosRepetidos.contains(numeros[i])) {
                        numerosRepetidos.add(numeros[i]);
                    }
                    break;
                }
            }
        }

        
        if (!numerosRepetidos.isEmpty()) {
            System.out.println("Los números repetidos son: " + numerosRepetidos);
        } else {
           
            System.out.println("No hay ningún número repetido");
        }
    }
}

```

2- 
```java
*
 * @author Miguel Angel
 */
public class Pruebas {
    public static int binarioADecimal(String binario) {
        int longitud = binario.length();
        int decimal = 0;

        for (int i = 0; i < longitud; i++) {
            
            char digito = binario.charAt(longitud - 1 - i);

           
            int valor = Character.getNumericValue(digito);

            
            decimal += valor * Math.pow(2, i);
        }

        return decimal;
    }

    public static void main(String[] args) {
        String numeroBinario = "1010";
        int numeroDecimal = binarioADecimal(numeroBinario);
        System.out.println("El número binario " + numeroBinario + " es igual a " + numeroDecimal + " en decimal.");
    }
}

```



