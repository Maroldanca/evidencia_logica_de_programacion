<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 

## Actividad: Ejecicios de métodos en Java
Resolver en parejas el ejercicio asignado por el docente

### Solucion

``` java
public static void main(String[] args) {
        int[] numerosPares = {2, 4, 6, 8, 10, 12};
        double mediana = calcularMediana(numerosPares);
        System.out.println("La mediana es: " + mediana);
    }

    public static double calcularMediana(int[] numeros) {
      
        Arrays.sort(numeros);

        int n = numeros.length;

        if (n % 2 == 0) {
            int medio1 = numeros[n / 2 - 1];
            int medio2 = numeros[n / 2];
            return (double) (medio1 + medio2) / 2.0;
        } else {
 
            return (double) numeros[n / 2];
        }
    }
```







