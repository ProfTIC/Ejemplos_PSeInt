

# **Índice**
- [Mostrar un valor por pantalla ](#mostrar-un-valor-por-pantalla)
- [Lectura de datos ](#lectura-datos)
- [Operadores ](#operadores)

# Mostrar un valor por pantalla <a name="mostrar-un-valor-por-pantalla"></a>

Para mostrar un mensaje por pantalla en java usa la siguiente instrucción:

```java
System.out.println("Hola mundo");
```
Si quieres mostrar el valor de una variable, se concatena con el operador +

```java
System.out.println("El valor de la variable es: "+variable);
``` 




# Lectura de datos<a name="lectura-datos"></a>

Usaremos la clase Scanner. Sigue los siguientes pasos:

1) Importa la librería:

```java
import java.util.Scanner;
```

2) Crea un objeto de dicha clase:

```java
Scanner sc = new Scanner(System.in);
```
En el ejemplo hemos usado el teclado (System.in)

3) Lee los datos. Dependiendo del tipo de dato, usaremos una instrucción u otra: 

```java
    nextByte() // para leer un dato de tipo byte.
    nextShort() //  para leer un dato de tipo short.
    nextInt()  // para leer un dato de tipo int.
    nextLong() // para leer un dato de tipo long. 
    nextFloat() //  para leer un dato de tipo float. 
    nextDouble() // para leer un dato de tipo double. 
    nextBoolean() //  para leer un dato de tipo boolean.
    nextLine()  // para leer un String hasta encontrar un salto de línea.
    next()  // para leer un String hasta el primer delimitador, generalmente hasta un espacio en blanco o hasta un salto de línea. 
```
Aquí tienes algunos ejemplos de código

```java
    int n;
    System.out.print("Introduzca un número entero: ");
    n = sc.nextInt(); //asigna a la variable n el número entero introducido por teclado  
    System.out.println("El número insertado es: "+n); // Muestra por pantalla el número que se acaba de insertar 
   
    String s;
    System.out.print("Introduzca el texto: ");
    s = sc.nextLine(); //asigna a la variable s el String introducido por teclado   
    System.out.println(texto); // Muestra el contenido del texto que se acaba de leer
```


Ejemplo completo

```java
import java.util.Scanner;  //importa la clase Scanner

public class EjemploLecturaDatosJava {

    public static void main(String[] args) {  

           Scanner sc = new Scanner(System.in);  //Se crea un objeto Scanner
           String nombre;
           int numero;

           System.out.print("Introduzca su nombre: ");       
           nombre = sc.nextLine();  //leer un String
           System.out.println("¡¡¡Hola " + nombre + "!!!");

           System.out.print("Introduzca un número entero: ");
           n = sc.nextInt(); //leer un entero
           System.out.println("El valor absoluto del número es: " + Math.abs(numero));
     }
}
```
  
  
  

# Operadores <a name="operadores"></a>

## Aritméticos

Tenemos la suma, resta, multiplicación y división (+, -, * y /). El operador módulo es %

Ejemplos: 
```java
suma = 6+4;               // Devuelve 10
resta = 8 - 2;            // Devuelve 6
multiplicacion = 5 * 2;   // Devuelve 10
division = 8 / 2;         // Devuelve 4
resto = 9 % 2;            // Devuelve 1
```

Si el operador / se aplica a dos números enteros (como en el ejemplo anterior), se obtiene el cociente de la división (un número entero). Si queremos que el resultado muestre decimales tenemos dos opciones: 
- Indicar que los dos números son de tipo decimal. Por ejemplo: 
```java
    System.out.println(5.0f/2.0f); // Se dividen dos números de tipo float
```
Si usamos variables sería: 
```java
    float a = 5.0f;
    float b = 2.0f;
    System.out.println(a/b);
```
- Usar un casting para forzar a que el resultado sea decimal. Por ejemplo: 
```java
    float resultado=(float) 5/2;
    System.out.println(resultado);
```

También se podría hacer usando dos variables de tipo entero: 
```java
    float resultado; 
    int num1 = 5;
    int num2 = 2;
    resultado =(float)num1/num2;
    System.out.println(resultado);
```
