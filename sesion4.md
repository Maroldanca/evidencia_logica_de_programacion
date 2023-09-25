<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4

## Actividad 4: Ejercicios de control de flujo con expresiones compuestas

```java
// Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;
```

Con la información anterior, implementa los siguientes ejercicios:

1. Determinar si el estudiante es mayor de edad y tiene un estado activo.
2. Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
3. Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
4. Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
5. Mostrar toda la información del estudiante si está matriculado en el Cesde.
6. Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
7. eterminar la cantidad de beca que recibe el estudiante según su promedio:

- 0.0 - 3.4: El estudiante no recibe beca.
- 3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
- 4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
- 4.5 - 5.0: El estudiante recibe una beca completa.

### Solucion

Aqui esta el algoritmo utilizado

```java
public class LPN1MR {

    public static void main(String[] args) {
        // Variables de tipo String
        String nombre = "Juan Pérez";
        String apellido = "González";
        String identificación = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
// Variable de tipo int
        int edad = 20;
// Variable de tipo boolean
        boolean esActivo = true;
        boolean becado = false;
// Variable de tipo char
        char género = 'M';
// Variable de tipo double
        double promedio = 4.5;
// Variable de tipo int
        int semestre = 2;
        
        System.out.println("---------------------------------");
        System.out.println("Ejercicio 1");
        
        if (edad >= 18 && esActivo){
            System.out.println("El estudiante es mayor de edad y es activo");
        } 
        
        System.out.println("---------------------------------");
        System.out.println("Ejercicio 2");
        
        if (becado || carrera.equals("Desarrollo de Software")){
            System.out.println("No es becado pero tiene carrera en desarrollo de Software");
        }
        
        System.out.println("---------------------------------");
        System.out.println("Ejercicio 3");
        
        if(semestre == 3 && esActivo){
            System.out.println("Cumple los 2 requisitos");
        } else {
            System.out.println("No cumple uno de los 2 requisitos");
        }
        
        System.out.println("---------------------------------");
        System.out.println("Ejercicio 4");
        
        if(carrera.equals("Desarrollo de Software") && (promedio > 4.0)){
            System.out.println("El estudiante tiene una carrera con Desarrollo y tiene un promedio superior a 4.0");
        }
        
        System.out.println("---------------------------------");
        System.out.println("Ejercicio 5");
        
        System.out.println("El estudiante " + nombre + " " + apellido + " Con numero de identificación " + identificación + ", Su corre es" + correo + "matriculado en la carrera " + carrera + " e inscrito en la universidad" + universidad);
        
        System.out.println("---------------------------------");
        System.out.println("Ejercicio 6");
        
        if(universidad.equals("Cesde") && (promedio > 4.0) && esActivo){
            System.out.println("Se le asigna una veca del 50%");
        }
        
        System.out.println("---------------------------------");
        System.out.println("Ejercicio 7");
        
        if(promedio == 4.5){
            System.out.println("El estudiante por tener un promedio de 4.5, recibe una beca completa");
        }
    }
```





