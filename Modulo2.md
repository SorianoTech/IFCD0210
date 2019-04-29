
# 2. Módulo 2: POO, Conceptos básicos I

## 2.1 Variables primitivas

En Java existen ocho tipos de datos primitivos que se pueden clasificar en:

- Números enteros (byte, short, int, long).
- Números reales (float, double).
- Carácter (char).
- Booleano o lógico (boolean).

## 2.2 Métodos

Métodos en Java. Un método en Java es un conjunto de instrucciones definidas dentro de una clase, que realizan una determinada tarea y a las que podemos invocar mediante un nombre. - System.out.println(); ... Este método es el punto de entrada al programa y también el punto de salida.

### Atributos o pripiedades

## 2.3 Clases

Normalmente en el mundo real existen varios objetos de un mismo tipo, o como
diremos enseguida, de una misma clase. Por ejemplo, mi bicicleta es una de las muchas
bicicletas que existen en el mundo. Usando la terminología de la programación
orientada a objetos, diremos que mi bicicleta es una instancia de la clase de objetos
conocida como bicicletas. Por lo tanto `Biciletas`(en plurar) seria la clase.

![clases](img\clases-en-Java3-1024x540.png)

>Es importante tener claro que una clase es una abstracción lógica.

```java
class NombreClase{
    //Declarar variables de instancia
    tipo var1;
    tipo var2;
    //..
    //Declarar métodos
    tipo metodo1(parámetros){
        //Cuerpo del método
    }
    tipo metodo2(parámetros){
        //Cuerpo del método
    }
}
```

[2]: https://www.arkaitzgarro.com/java/capitulo-9.html

## 2.4 Arrays y otros componentes

## 2.5 Funciones de cadena

Metodos de la clase String

### Metodo Lenght

Métodos:

- `Lenght()`: devuelve un entero que representa la longitud de la cadena.
- `charAt(int)`: devuelve el caracter que esta en la posición.
- `toUpperCaser()`: convierte la cadena a mayusculas
- `toLOwerCaser()`: convierte la cadena a minusculas.

## 2.6 Estructuras de control de flujo

**Alternativas**

1. Simple
if, else if
```
si (condicion)
    acciones
fin-si
```

2. Compuesta

If, else if, else if 

```console
si (condicion)
    accion 1
si no
    accion 2
fin-si
```

3. Multiple

Solo se va a ejecutar uno de todos los casos posibles. (Switch)

``` 
caso (valor variable)
    caso 1: acción 1
    caso 2: accion 2
    caso n: accion n
fin-caso
```

**Repetitivas**

Bucles while, for, do while

- Conocemos Nº Repeticiones
```
desde (inicion hasta fin)
    acciones
fin-desde
```

- No Conocemos Nº Repeticiones

While: se ejecuta de 0 a N veces

```
mientras (condicion)
    accion
fin de concion
```

do while : se ejecuta de 1 a N veces. 
```
hacer
    accion | es
fin-hacer(condicion)
```

## 2.7 Condicional if

Alternativa simple 

```java
if (condicion) {
  // la condicion se cumple si la condicion es verdadera
  accion/es;
}
```

Alternativa compuesta

```java
if (condicion) {
  // la condicion se cumple si la condicion es verdadera
  accion/es;
} else {
    accion2;
}
```

**Operadores relacionales** son aquellos que se utilizan dentro de las condiciones.

| Operador  |  Utilización |  Resultado |
|---    |   ---            |           ---|
|  > | A > B  | verdadero si A es mayor que B  |
|  >=  | A >= B  | verdadero si A es mayor o igual que B  |
| <  |  A < B | verdadero si A es menor que B  |
|  <= | A <= B  |  verdadero si A es menor o igual que B |
|  == | A == B  | verdadero si A es igual a B  |
|  != |  A != B |  verdadero si A es distinto de B |

## 2.8 Condicional switch

La sentencia de switch sirve para elegir una opcion según la entrada de una expresión. Este tipo de sentencia se pueden utilizar las palabras clave `break` y `default`.

`break`: nos permite salir del bucle en caso de que se cumple el caso. Cualquier opción que no se la ultima opción necesita llevar un break.
`default`: sirve para que cuando ninguno de los casos que tenemos definidos sea introducido se ejecute esa orden. (No necesita break). Solo lleva break en caso de que no sea la ultima opción

Una vez que se ha evaluado la expresión se comprueba si coincide con alguno de los valores de case. En caso de que se cumpla, ejecuta el codigo que esta dentro de ese apartado hasta encontrar una sentencia break. Si no utilizamos la sentencia `break` seguira intentando buscar opciones disponibles en los case y nos puede ocasionar problemas en nuestro programa.

```java
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

## 2.9 Bucle while y do while

### While
El bucle while realiza la operación del código hasta que la condición sea verdadera.

En el siguiente flujograma podemos ver como se ejecutan las accciones.

![while](img\bucle_while.png)

Sintaxis:

```java
while (condicion){
    bloque-de-sentencia;
}
```

### Do while

La diferencia entre el while es que en este caso, primero se realizar el bloque de sentencias que esta dentro del do y luego comprueba la condición.

Sintaxis:

```java
inicializacion;
do{
bloque-de-sentencias;
} while (condición);

```

Ejemplo do while:

```java
int i = 0;
do {
  System.out.println(i);
  i++;
}
while (i < 5);
```

## 2.10 Bucle for clásico

Es una estructura repetitiva en la cual sabemos el numero de repeticiones.

```java
for(iniciaicion;condicion;incremento)
    {
        accion/es;
    }
```

Ejemplo:

```java
for (int i = 0; i < 5; i++) {
  System.out.println("Valor de i="+i);
}

```


## 2.11 Bucle foreach

Nos sirve para recorrer un bucle segun los elementos que contenga una array.

```java
for (type variable : arrayname) {
  // code block to be executed
}
```

Ejemplo:
```java
String[] coche = {"Opel", "Renault", "Toyota", "Citroen"};
for (String i : coche) {
  System.out.println(i);
}
```

**Ejercicio 1**

Realizar un programa que imprima los 20 primeros numeros pares incluyendo el 20.

```java
for (int i = 0; i <= 20; i = i + 2) {
  System.out.println(i);
}
```

**Ejercicio 2**

Calcula la suma de los numeros pares entre 0 y 20.

```java
//Calcula la suma de los numeros pares entre 0 y 20.
int num = 20, i, total = 0;
for(i = 0; i <= num; i+=2){
    total = total + i;
}

System.out.println("La suma de los 20 numeros pares es: "+total);
```

PSEUDOCODIGO

```
desde i=0 hasta i<=20 incremento 2
    suma = suma +
fin-desde

imprimir suma
```

**Ejercicio 3**

Imprimir los numeros impares del 15 al 1

```java
for (int i = 15; i > 0; i = i -2 ) {
    System.out.println("El número impar es: "+i);
}
```

### Operadores Aritméticos

|  OPERADOR |  DESCRIPCIÓN |
|---        |           ---|
|  + |  Suma |
|  - |  Resta |
|  * |  Multiplicación |
|  / | division entera (4/3 devuelve 1)  |
|  % | Resto de una división entre enteros   |

Destacar que el operador % es de uso exclusivo entre enteros. 7%3 devuelve 1 ya que el resto de dividir 7 entre 3 es 1. Al valor obtenido lo denominamos módulo (en otros lenguajes en vez del símbolo % se usa la palabra clave mod) y a este operador a veces se le denomina "operador módulo".

### Operadores Lógicos


Operador| Descripción |
---------|----------|
 == | Es igual | 
 != | Es distinto |
 <, <=, >, >= | Menor, menor o igual, mayor, mayor o igual | 
 && | operador and (y)
 `||` | operador or (o)
 ! | operador not(no)

**Ejercicio 4**

Imprimir los pares entre 20 utilizando el operador %
```java
//define limit
int limit = 20;
for(int i=1; i <= limit; i++){
  if(i % 2 == 0){
    System.out.print(i + " ");
    }
}
```

**Ejercicio 5**

Imprimir la tabla de multiplicar del 9
0 x 9 = 0
1 x 9 = 9

```java
int number = 9;
  for (int i=1; i<=10; i++){
     System.out.println(number + " x " + i + " = " + number*i);
  }
```

**Ejercicio 6**

Realizar un Pseudocodigo y un programa JAVA basado en ese pseudocódigo para calcular si el número 2399 es o no primo, y en caso de que no lo sea decir cuantos (no cuales) son sus divisores.

Nota: Un número primo es aquel que solamente es divisible por sí mismo y por unidad.

Ejemplo: El 7 es un número primo.

El número 8 no es primo y tiene 2 divisiores (el 2 y el 4)


```console
INICIO
definir numero = 2399
definir contador = 0
PARA numero si (si el cociente es igual a 1 y )
{
  Imprimo el numero primo
}si no
{

}

FIN
```

```java
public class primos
{
    public static void main(String[] args)
    {
        int numero = 2037;
        int contador = 0;
        for(int i = numero; i > 0; i--){
            if(numero % i == 0 ){
                contador++;
                System.out.println("Los números divisores son: "+ i);
            }
        }
        System.out.println("El número "+ numero + " tiene "+ contador +" divisores");
        if(contador==2){
            System.out.println("El número es primo");
        }else{
            System.out.println("El número NO es primo");
        }
    }
}
```

**Ejercicio 7**

Realizar un Pseudocodigo y un programa JAVA basado en ese pseudocódigo para calcular el factorial del número 9.

Nota: El factorial del 5 e 5 x 4 x 3 x 2 x 1 es decir 120.

```java
public class factorial {
    public static void main(String[] args)
    {
        double factorial = 1;
        // El número elegido para el factorial es el 5
        double numero=5;
        while (numero!=0)
        {
            factorial=factorial*numero;
            numero--;
        }
         System.out.println("El factorial es: "+ factorial)
    }
```

**Ejercicio 8**

Realizar un programa de JAVA que dibuje lo siguiente

```console
*
 *
  *
   *
    *
```

```java
public class asterisco {
    public static void main(String[] args) 
    {
        String texto="";
        for (int i = 0;i<5;i++)
        {
           System.out.println(texto + "*");
           texto = texto + " ";
        }
    }
}

```