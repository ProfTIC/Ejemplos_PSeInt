aEn java tenemos las siguientes estructuras condicionales: 

- [Estructura if](#if)
- [Estructura if ... else](#ifelse). 
- [Estructura if ... else if](#ifelseif)
- [Estructura if anidados](#ifanidados)
- [Instrucción switch](#switch)


# Estructura if <a name="if"></a>

Es la más sencilla de todas las opciones. Es equivalente a si (condición) entonces. 

La sintaxis es la siguiente: 

```java
    if (condición) {

        instrucciones_si_condición_es_cierta

    }

    // Si solo hay una única instrucción no es necesario poner las llaves {}

    if (condición) 

        instrucciones_si_condición_es_cierta

    // En este caso la escritura puede ser más compacta porque podemos poner la instrucción a continuación de la condición: 

    if (condición) instrucciones_si_condición_es_cierta
```
Por ejemplo:

```java
    // Usando llaves

    if (num < 10) {
               
        System.out.println("El número es menor que 10");

    }
    // El mismo ejemplo anterior pero sin usar llaves (solo hay una única instrucción)
    
    if (num < 10) 
               
        System.out.println("El número es menor que 10");

    // Con una sintaxis compacta
    
    if (num < 10) System.out.println("El número es menor que 10");
    
```

# Estructura if ... else <a name="if"></a>

Es similar a la anterior, pero incluyendo la parte si_no. Es decir, en este caso hay que ejecutar instrucciones tanto si se cumple la condición del if como si no se cumple. 

La sintaxis es la siguiente:

```java
    if (condición) {

        instrucciones_si_condición_es_cierta

    } else {

        instrucciones_si_condición_es_falsa
    }

    // Si solo hay una única instrucción no es necesario poner las llaves {}

    if (condición) 

        instrucciones_si_condición_es_cierta

    else

        instrucciones_si_condición_es_falsa

    // Puede ocurrir que una parte tenga más de una instrucción y sea necesario usar las llaves y en otra no. Por ejemplo: 

    if (condición) {

        instrucciones_si_condición_es_cierta

    } else

        instrucciones_si_condición_es_falsa

    // Si hay más de una instrucción en la parte falsa pero solo una en la cierta sería: 

    if (condición) 

        instrucciones_si_condición_es_cierta

    else {

        instrucciones_si_condición_es_falsa
    
    }

    // Generalmente la parte que tiene menos instrucciones suele incluirse en la condición verdadera. Por tanto, el código más extenso se quedaría en la parte de la condición cuando es falsa
```
Por ejemplo:

```java
    // Usando llaves

    if (num < 10) {
               
        System.out.println("El número es menor que 10");

    } else {

        System.out.println("El número es mayor o igual que 10");

    }
   
    // El mismo ejemplo anterior pero sin usar llaves (solo hay una única instrucción)
    
    if (num < 10) 
            
        System.out.println("El número es menor que 10");

    else 

        System.out.println("El número es mayor o igual que 10");

    // Ejemplo combinando una parte con llaves y otra sin llaves   

    if (num < 0) 
            
        System.out.println("No se puede calcular la raíz de un número negativo");

    else {

        raiz = Math.sqrt(num);

        System.out.println("La raiz de "+num+" es: "+raiz);
    }
```

Existe una opción más corta para crear un código if...then...else y es usar el operador ternario ? que permite establecer la condición y qué instrucciones se ejecutarán si se cumple o no. 

La sintaxis básica es la siguiente: 

```java

    resultado=condición?valor_cumple_condición:valor_no_cumple_condición

```
La estructura quedará más clara si vemos un ejemplo. Imaginemos que queremos guardar en una variable menor cuál es el número menor entre dos valores num1 y num2. Si usamos la estructura if el código sería: 

```java

    if (num1 < num2)

        menor=num1;

    else

        menor=num2;

```
Este código usando el operador ternario ? sería: 

```java

    menor=num1<num2?num1:num2;

```

# Estructura if ... else if <a name="if"></a>

La siguiente opción que tenemos es incluir una condición en la parte else para que se compruebe en caso de que no se cumpla la principal. 

La sintaxis es la siguiente: 

```java
    if (condición) {

        instrucciones_si_condición_es_cierta

    } else if (condición2) {

        instrucciones_si_condición2_es_cierta
   
    } else {
  
        instrucciones_si_todas_condiciones_son_falsas
  
    }
```

Hay que tener en cuenta algunas consideraciones: 
- El funcionamiento de las llaves es igual al que se ha descrito anteriormente. Es decir, son opcionales si engloban a un bloque de una única instrucción
- La parte else final es opcional. Solo la incluimos si realmente se necesita

Vamos a ver un ejemplo: 

```java
// Este programa muestra si un número es menor, mayor o igual a cero

    if (num < 0) 
            
        System.out.println("El número es menor que 0");

    else if (num=0)

        System.out.println("El número es igual a cero");
    
    else

        System.out.println("El número es mayor que cero");
```

También podemos escribir el código anterior usando llaves: 

```java
// Este programa muestra si un número es menor, mayor o igual a cero

    if (num < 0) {
            
        System.out.println("El número es menor que 0");

    } else if (num=0) {

        System.out.println("El número es igual a cero");
    
    } else {

        System.out.println("El número es mayor que cero");

    }
```

# Estructura if anidados <a name="ifanidados"></a>

Java permiter anidar condiciones, incluyendo estructuras condicionales if dentro de otras. No existe ninguna limitación a la hora de combinar las diferentes instrucciones.

Por ejemplo, el siguiente programa muestra el número que se ha insertado. Nos puede servir como base para crear un menú de opciones: 

```java
// Este programa muestra un menú con diferentes opciones e indica cuál se ha seleccionado

        Scanner sc = new Scanner(System.in);
        int opcion;

        System.out.println("Seleccione la opción que desee");
        System.out.println("1. Suma");
        System.out.println("2. Resta");
        System.out.println("3. Producto");
        System.out.println("Pulse cero para salir");

        opcion = sc.nextInt();

        if (opcion == 0) {

            System.out.println("Has elegido salir");

        } else if (opcion == 1) {

            System.out.println("Has seleccionado la suma");

        } else if (opcion == 2) {

            System.out.println("Has elegido la opción 2: la resta");

        } else if (opcion == 3) {

            System.out.println("La opción elegida es la 3: el producto");

        } else {

            System.out.println("Opción no válida");
        }
```

Hay que tener en cuenta que cuando anidamos muchas estructuras condicionales puede ocurrir que el código sea ambiguo y no resulte claro a qué condición hace referencia cada else. Este problema se denomina *dangling else* y puedes ver un ejemplo en esta <a href="https://en.wikipedia.org/wiki/Dangling_else">página </a>

# Instrucción switch <a name="switch"></a>

Esta instrucción permite implementar programas que anidan diferentes instrucciones. Generalmente la solución con *switch* suele ser más legible que cuando usamos varios if anidados. 

La sintaxis básica es la siguiente: 

```java
    switch (variable) {

        case valor_1: 
        
            //Instrucciones si variable == valor_1
            
            break; // La instrucción break hace que salgamos del switch. Si no se incluye, aunque se cumpliera la condición de que variable=valor_1, se seguirían comprobando el resto de opciones
        
        case valor_2: 
        
            //Instrucciones si variable == valor_2

            break;
     
        case valor_3: 
     
            //Instrucciones si variable == valor_1

            break;

        default: 
            // Instrucciones que se ejecutan si no se cumple ninguna de las condiciones anteriores
    }
```

A continuación se muestra el ejemplo anterior del menú usando la estructura switch: 

```java
        
    Scanner sc = new Scanner(System.in);
    int opcion;

    System.out.println("Seleccione la opción que desee");
    System.out.println("1. Suma");
    System.out.println("2. Resta");
    System.out.println("3. Producto");
    System.out.println("Pulse cero para salir");

    opcion = sc.nextInt();

    switch (opcion) {

       case 0:

            System.out.println("Has elegido salir");

            break; // No queremos que se compruebe ninguna opción más: por eso se indica que finalice la ejecución del switch

        case 1:

            System.out.println("Has elegido la suma");

            break;

        case 2:

            System.out.println("Has elegido la resta");

            break;

        case 3:

            System.out.println("Has elegido el producto");

            break;

        default:

            System.out.println("Opción errónea");

    }

```
Esta estructura puede escribirse también como *rule switch* o *switch extendido*, que elimina la necesidad de usar la instrucción break. Sería: 

```java
    switch (opcion) {

        case 0 -> System.out.println("Has elegido salir");
            
        case 1 -> System.out.println("Has elegido la suma");

        case 2 -> System.out.println("Has elegido la resta");

        case 3 -> System.out.println("Has elegido el producto");

        default -> System.out.println("Opción errónea");

    }
```
