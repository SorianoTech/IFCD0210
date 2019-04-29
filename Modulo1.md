# Módulo 1. Contexto e introducción al curso

## 1.1 ¿Qué es la programación y en que sitios está presente?

La programación viene del verbo programar, que en el ambito tecnólogico significa, segun la RAE:

>Cada una de las operaciones que, en un orden determinado, ejecutan ciertas máquinas.

Hoy en día la programación esta en practicamente todos los
ambitos de nuestra vida, desde la medicina, hasta la agricultura o desde la aeronautica hasta los equipos que funcionan en los submarinos, desde las web donde compramos como amazon, hasta la información que consultamos y tramitamos en hacienda. Cualquier cosa que requiera de un procesamiento de datos, intercambio de información entre personas ubicades en diferentes lugares o equipos que requieran de calculos matémáticos tendrán presente la programación.

Es por este motivo que aunque hoy en día existen multitud de campos en donde se esta aplicando la programación, hoy en día sigue en crecimiento debido al aumento de la tendencia de utilizar dispositivos electronicos e internet en nuestra vida cotidiana.

![Uso de internet](img\Grafica-2-usuarios-internet-incremento-con-los-años.jpg)
*Uso de internet en los ultimos años

### Ejemplo de programación en java:

```java
public class A {
    
    public Integer numeroEntero = new Integer(); /* Variable Global a todos los Métodos */
    
    public Integer metodo() {
        int num = 1; // Variable Local a método. Puede accederse dentro de este método en cualquier parte, pero no fuera del mismo.
        for (int i = 0;i<numeroEntero.intValue();i++) { // i es local al bucle for, sólo puede ser accedida dentro del mismo.
            num *= i;
        }
        // i = 2; Esta línea provocaría error al no haber declarado la variable i. i fue definida localmente al bucle for.
        return Integer.valueOf(num);
    }

    public void otroMetodo() {
        int num = 1; // Variable local a otroMetodo. num aquí es una variable distinta a la variable num de método
        System.out.println("Variable local num: " + num);
    }
}
```

## 1.2 Distintas modalidades y carreras profesionales

Para poder entender la programación podriamos dividirla en diferentes modalidades o carrereas profersionales pero antes podemos realizar

Segun su paradigma:

- Imperativa
  - Estructurados
  - Procedimental
  - OOP (Orientada a objetos)
  - otros
- Declarativa
  - Funcional/estructurado
  - Lógico
  - Otros

Segun su interpretación:

- Interpretados
- Compilados

La principal diferencia entre un **lenguaje compilado** y uno **interpretado** es que el lenguaje compilado requiere un paso adicional antes de ser ejecutado, la compilación, que convierte el código que escribes a lenguaje de máquina. Un lenguaje interpretado, por otro lado, es convertido a lenguaje de máquina a medida que es ejecutado.

>Los lenguajes compilados transforman el código fuente en codigo máquina.

Un **lenguaje de programación** es un idioma artificial diseñado para expresar procesos que pueden reproducir máquinas. Se usan para crear programas que controlan el comportamiento físico y lógico de una máquina y para expresar algoritmos con precisión. Los llamamos lenguaje porque están formados por un conjunto de símbolos, reglas sintácticas y semánticas que definen su estructura y el significado de los elementos y expresiones.

![Lenguajes de Programación](img\Grafica-2-usuarios-internet-incremento-con-los-años.jpg)

### Carreras profesionales

En el ambito de la programación podemos diferenciar las siguientes especialidades:

- Fron-End
- Back-End
- Dev-Ops
  
## 1.3 Concepto general de Programación Estructurada

Para realizar un programa estructurado existen tres tipos básicos de estructuras de
control:

- `Secuencial`: Ejecuta una sentencia detrás de otra.
- `Condicional`: Se evalúa una expresión y, dependiendo del resultado, se decide la
siguiente sentencia a ejecutar. (If, else if, switch)
- `Iterativa o bucle`: Repetimos un bloque de sentencias hasta que sea verdadera una
determinada condición. (do, while, for, do while)

En los avances de la programación estructurada aparecen la creación de módulos que consisten en agrupación de codigos que componen librerias. Estas librerias nos permiten ahorrarnos escribir de nuevo un código que puede ser reutilizado.

Por ejemplo para definir un programa de ajedrez lo podemos dividir en 3 modulos:

- Ajedrez
- Tablero
- Pieza

El contenido del fichero de libreríatablero.h sería:

```c
enum columnas { a, b, c, d, e, f, g, h };
struct tablero {
    int posx;
    enum columnas posy;
    struct pieza mipieza;
    struct tablero *siguiente;
}

int Final(struct tablero *mitablero);
void Inicio(struct tablero *mitablero);
int Pertenece(struct tablero *mitablero, int posx, enum columnas posy);
void Dibuja(struct tablero *mitablero);
int FueraTablero(struct tablero *mitablero, int x1, enum columnas y1, int x2, enumcolumnas y2);
int Valido_T(struct tablero *mitablero, int x1, enum columnas y1, int x2, enum columnas y2);

void Mover(struct tablero *mitablero, int x1, enum columnas y1, int x2, enum columnas y2);
```
[1]: bibliografia\programacion_estructurada.pdf

El fichero de declaración pieza.h incluiría el siguiente código:

```c
enum color { blanco, negro };
enum tipo { peon, torre, caballo, alfil, reina, rey }
struct pieza {
enum color micolor;
enum tipo mitipo;
}
int Valido_P(struct pieza *mipieza, int x1, int y1, int x2, int y2);
```

Al incluir los ficheros tablero.h y pieza.h podemos usar las funciones de los modulos a pesar de no conocer el código interno, solo debemos conocer como funcionan los objetos para utilizarlos.

## 1.4 Concepto general de Programación Orientada a Objetos

En el caso de los lenguajes orientados a objetos, como es el caso de C++ y Java, el
elemento básico no es la *función*, sino un ente denominado precisamente *objeto*. Un
objeto es la representación en un programa de un concepto, y contiene toda la
información necesaria para abstraerlo: datos que describen sus atributos y operaciones
que pueden realizarse sobre los mismos.

Los niveles de abstracción del POO son:

- Poliformismo
- Herencia
- Encapsulación
- Abstraccion
- Clases
- Objetos
- Metodos
- Paso de Mensajes

![abstraccion](img\OOPs-Concepts.jpg)

[Ejemplos](https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/)

[2]: https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/

Los veremos explicados más adelante.

### Objeto

Un *objeto* no es más que un conjunto de variables (o datos) y métodos (o funciones)
relacionados entre sí. Los objetos en programación se usan para modelar objetos o
entidades del mundo real (el objeto hijo, madre, o farmacéutica, por ejemplo). Un objeto
es, por tanto, la representación en un programa de un concepto, y contiene toda la
información necesaria para abstraerlo: datos que describen sus atributos y operaciones
que pueden realizarse sobre los mismos. La siguiente figura muestra una representación
visual de un objeto.

![Clases y Objetos](img\objetos_clases.jpg)

[2]: bibliografia\ProgramacionOrientadaAObjetos.pdf

## 1.5 Programación Estructurada vs Programación Orientada a Objetos

La principal diferencia entre la estructurada y la orientada a objetos consiste en la forma en la que abstraemos los datos. La estructurada realizar una serie de ordenes de forma ordenada y no es posible acceder a datos predefinidos.

La programación orientada a objetos es mas avanzada ya que nos permite 

## 1.6 El proyecto CODE.ORG

Variables

Variable
Variable local
Variable global
Variable estática
Variable externa
Variable de instancia
Variable de clase
Variable de entorno

## Recursos de estudio gratuitos

[CodeAcademy](http://www.codecademy.com/#!/exercises/0)

[Google Code University](http://code.google.com/edu/)

[Mozilla Developer Network](https://developer.mozilla.org/en-us/learn)

[Khan Academy](https://www.khanacademy.org/cs/tutorials/programming-basics)

[EloquentJavascript](http://eloquentjavascript.net/)

[Codeschool](http://www.codeschool.com/)