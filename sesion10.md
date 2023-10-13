<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 

## Actividad: Prueba, ejecución y explicación de ejercicios de lógica de programación.

Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno

## Solucion

### Calcular el movimiento rectilinio uniforme
```java
import java.util.Scanner;

public class MRU {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double velocidad, tiempo, distancia;
      
      // Solicita la velocidad y el tiempo
      System.out.print("Ingrese la velocidad en metros por segundo: ");
      velocidad = input.nextDouble();
      System.out.print("Ingrese el tiempo en segundos: ");
      tiempo = input.nextDouble();

      // Calcula la distancia recorrida
      distancia = velocidad * tiempo;

      // Muestra el resultado en la consola
      System.out.printf("La distancia recorrida es de %.2f metros.", distancia);
   }
}
```

#### Explicacion
El movimiento rectilinio uniforme se calcula con la formmula de
distancia = velocidad x tiempo. Entonces empezamos con un scanner input y unas variables tipo double que se llamaran: Velocidad, tiempo y distancia. Luego se le pedira al usuario que ingrese la velocidad en metros por segundo y se almacenara en velocidad, luego que ingrese el tiempo en segundos y se almacenara en tiempo. De aqui se hara la operacion en donde la variable distancia, almacenara el resultado de la operacion: Velocidad * tiempo, y luego un System.out.printf, regresara el resultado con una cadena de texto que es "La distancia recorrida es de %.2f metros.", distancia"


###  Cálculo del costo de energía eléctrica de un electrodoméstico

```java
import java.util.Scanner;

public class CalculoCostoEnergiaElectrica {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      // Solicitar datos al usuario
      System.out.print("Ingrese la potencia del electrodoméstico (en vatios): ");
      double potencia = input.nextDouble();
      
      System.out.print("Ingrese el tiempo de uso diario (en horas): ");
      double tiempoUsoDiario = input.nextDouble();
      
      System.out.print("Ingrese el precio por kilovatio-hora (en pesos): ");
      double precioKwh = input.nextDouble();
      
      System.out.print("Ingrese el número de días del mes: ");
      int diasDelMes = input.nextInt();
      
      // Cálculo del consumo mensual en kilovatios-hora
      double consumoDiarioKwh = (potencia * tiempoUsoDiario) / 1000;
      double consumoMensualKwh = consumoDiarioKwh * diasDelMes;
      
      // Cálculo del costo mensual de energía eléctrica
      double costoEnergiaElectrica = consumoMensualKwh * precioKwh / 1000; // se divide entre 1000 para convertir el precio por kilovatio-hora en pesos
      
      // Imprimir el resultado en pantalla
      System.out.printf("El costo mensual de energía eléctrica es de: $%,.2f pesos", costoEnergiaElectrica);
   }
}
```

#### Explicacion
Primero se debe conocer el costo de energia de un electrodomestico, sabiendo la potencia en vatios y el tiempo de uso diaro de ese electrodomestico en horas. De aqui vamos al algoritmo que tendra un scanner input y varias variables que se iran explicando. Se empieza con un Systemprintf que pedira al usuario ingresar la potencia del electrodomesticos y se almacenara en la variable double potencia, luego pedira el tiempo de uso en horas y se almacenara en la variable double tiempoUsoDiario, despues pedira el precio por kilovatios-hora en pesos y se almacenara en la variable double precioKwh y por ultimo pedira el numero de dias del mes y se almacenara en la variable entero diaDelMes. Y luego se crearan 3 variables tipo double que almacenaran lo siguiente: consumoDiarioKwh que guardara el resultado de la operacion de (potencia * tiempoUsoDiario) / 1000, luego el consumoMensualKwh que guardara el resultado de la operacion de consumoDiarioKwh * diasDelMes y por ultimo costoEnergiaElectrica que guardara el resultado de la operacion consumoMensualKwh * precioKwh / 1000 y se divide entre 1000 para convertir el precio por kilovatio-hora en pesos. Y por entrega final, se imprimira un Systemprintf que retornara el costoEnergiaElectrica 





