En java tenemos los siguientes bucles o sentencias repetitivas:

- [For (para)](#for)
- [While (mientras)](#while). 
- [Do-While (hasta)](#dowhile)



# For (para) <a name="for"></a>

Esta sentencia es similar a la de otros lenguajes de programación y se basa en los tres componentes básicos de cualquier bucle para: 
- Inicio: la variable centinela o contador se inicializa con un determinado valor
- Condición de fin: el bucle parará cuando se cumpla esta condición
- Modificación de la variable centinela: cómo cambia el valor de la variable en cada iteración del bucle

La sintaxis es la siguiente: 

```java
    
    for(int i = valor_inicial; i <= valor_final; i = i + paso) {

        // Si solo hay una única instrucción no es necesario poner las llaves {}

    }

   
```


Por ejemplo:

```java
    
    for(int i=0;i<2;i++) {

        System.out.println("El valor de la variable contador es: ",i);
    }

```

Si ejecutamos paso a paso el código anterior tenemos los siguientes resultados: 

1. Primero se inicializa la variable i y toma el valor de 0
2. Se comprueba la condición de fin (i<2). Como la condición se cumple, se entra en las instrucciones del bucle
3. Se ejecuta la instrucción ```System.out.println``` y se muestra por pantalla el valor de la variable i (en este caso se mostraría el valor 0)
4. Se ejecuta la instrucción de modificación de la variable contador (i++). Por tanto, i valdrá 1
5. A continuación, se vuelve a comprobar la condición de fin (i<2). Como se sigue cumpliendo, se entra en las instrucciones del bucle
6. Se ejecuta la instrucción ```System.out.println``` y se muestra por pantalla el valor de la variable i (en este caso se mostraría el valor 1)
7. Se ejecuta la instrucción de modificación de la variable contador (i++). Por tanto, i valdrá 2
8. A continuación, se vuelve a comprobar la condición de fin (i<2). Como no se cumple, la ejecución del bucle finaliza

En la siguiente tabla tenemos un resumen de la traza del algoritmo: 

| Nº instrucción | Instrucción | Valor de la variable i | Observaciones | Salida por pantalla |
| :---------:|------------ |---------| ---------|---------|
| 1 | i=0 | 0 | | |
| 2 | ¿i<2? | 0 | Como se cumple la condición, se ejecuta la instrucción del bucle| |
| 3 | System.out.println | 0 | | El valor de la variable contador es 0
| 4 | i++ | 1 | ||
| 5 | ¿i<2 | 1 |Como se cumple la condición, se ejecuta la instrucción del bucle| |
| 6 | System.out.println | 1 |  | El valor de la variable contador es 1
| 7 | i++ | 2 | | |
| 8 | ¿i<2 | 1 |Como no se cumple la condición, la ejecución del bucle finaliza| |

# While (mientras) <a name="while"></a>

Este tipo de bucle se ejecuta mientras se cumpla la condición establecida en la instrucción while. Por tanto, las instrucciones del bucle se ejecutarán mientras la condición de parada sea cierta

La sintaxis es la siguiente: 

```java
    
   while (condición_parada) {

        // Si solo hay una única instrucción no es necesario poner las llaves {}

    }

   
```


Por ejemplo:

```java

    int i=0;
    
    while (i < 2) {

        System.out.println("El valor de la variable i es: " +i);

        i++;
    }

```

El código anterior es equivalente al bucle for que hemos visto. En este caso, las instrucciones del bucle se ejecutan mientras se cumpla que i<2. La sentencia i++ actualiza el valor del contador en cada ejecución del bucle

# Do-While (hasta) <a name="dowhile"></a>

Este tipo de bucle es parecido al anterior, pero la condición de parada se comprueba después. Es decir, si usamos una estructura do-while el cuerpo del bucle se **ejecutará al menos una vez**. 

La sintaxis es la siguiente: 

```java

    do {

        // Instrucciones
    
    } while (condición_parada) {

```


Por ejemplo:

```java

    int i=0;

    do {

        System.out.println("El valor de la variable i es: "+i);

        i++;
    
    } while (i < 2);

```
Este código es equivalente a los dos ejemplos de los bucles anteriores. La diferencia con la estructura while es que la condición se evalúa después de ejecutar una vez las sentencias del bucle. En este caso, independientemente del valor de i, la instrucción System.out.println y la de i++ se ejecutarán al menos una vez