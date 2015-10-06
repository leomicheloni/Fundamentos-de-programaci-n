# Fundamentos de programación

Éste es un pequeño resumen sobre conceptos de programación en el cual se han simplificado muchos conceptos para facilitar la comprensión y hacerlo más compacto.

[¿Cómo está orgranizado esto?](organizacion.md)

##Qué es un programa?

Un programa es la forma en que le decimos a una computadora qué queremos que haga, paso a paso, con instrucciones simples, del mismo modo que cocinar es seguir una receta, un programa le dice a la computadora qué queremos que haga siguiendo un conjunto de pasos.

##Qué es un lenguaje de programación?

Las computadores no entienden nuestro lenguaje sino que utilizan algo conocido como "código máquina" (básicamente unos y ceros), un lenguaje de programación nos permite expresar aquello que queremos hacer de un modo comprensible por nosotros siguiendo ciertas reglas, luego es convertido a código máquina por un programa llamado "compilador". 
En este caso utilizaremos C# como lenguaje.

Desde un punto de vista práctico existen 4 elementos principales en la programación tradicional:

- [Variables](#variables)
- [Decisiones, control de flujo](#decisiones)
- [Repeticiones](#repeticiones)
- [Funciones o rutinas](#functiones)

##Variables

Las variables son lugares en donde dejamos valores para utilizarlos después, por ejemplo, si queremos guardar un número de teléfono lo podemos dejar en una variable y luego recuperarlo.
````csharp
int telefono;         //reservamos un lugar en la memoria RAM de la computadora y le llamamos "telefono"
telefono = 123123; //colocamos el valor 123123 en ese lugar de memoria
````
(El texto después de las dobles barras "//" es un comentario y no es tenido en cuenta por C#)

Algunas cosas más sobre variables:
- Tienen un nombre único que las identifica (dentro del contexto en que están)
- La acción de "guardar" un valor dentro a una variable se conoce como "asignación"

En el ejemplo anterior asignamos el valor 123123 a la variable "telefono", a partir de ahora podemos recuperar ese valor en otra parte de nuestro programa y, por supuesto, podemos cambiarlo cuando queramos.

````csharp
telefono = 1123123; //cambiamos el valor anterior
`````

En este ejemplo cambiamos el valor de la variable "telefono", nótese que ya no usamos la palabra "int" delante, la misma sólo se utiliza al momento de declarar la variable.

## Tipos de variables

En el ejemplo del teléfono simplemente guardamos el valor y ya, esto reserva un lugar en memoria para nuestra variable, pero también indicamos "int" cuando la declaramos, esto es porque existen diferentes tipos de variables, es decir, no es lo mismo guardar un texto como "hola mundo" a guarda un número como "123123", nosotros tenemos que indicar a C# qué tipo de valor vamos a guardar en esa varible.
Los tipos más comunes son:

- Enteros: int
- Cadenas de texto: string
- Números con punto flotantes (decimales): double
- Booleanos (true o false): bool

Existen otros tipos pero por ahora vamos a utilizar estos.
````csharp
int edad = 12;
string nombre = "Leonardo"; //las cadenas de texto se escriben entre comillas dobles
double altura = 1.74; //en C# se utiliza el punto "." para separar los decimales
bool casado = true; //los booleanos toman dos posibles valores "true" o "false"
````
Existen expresiones que se utilizan con las variables que pueden ser confusas (o matemáticamente extrañas) pero son bastante comunes, un caso típico es cuando queremos utilizar una variable para contar, es decir la variable tiene el valor 0 y lo queremos incrementar cada vez que algo ocurre, eso se escribiría así:

````csharp
int contador = 0; //declaramos la variable y le asignamos un valor inicial
contador = contador +1; //matemáticamente es incorrecto, pero en programación es común decir "al valor que tenía antes sumar 1"
````
Esto mismo se puede resumir así:
````csharp
int contador = 0;
contador++; //significa: agregar 1 al valor anterior de la variable contador
````
[Más sobre variables en C#](variables.md)

##Decisiones
Las decisiones son estructuras de control de flujo, es decir permiten decidir si hacer una cosa u otra dependiendo de ciertas circunstancias.
La estructura de control más utilizada es "if" que significar algo como "si se cumple cierta condición hacer esto", por ejemplo:

````csharp
int edad = 12;
if(edad > 17){
  //en esta parte hacemos algo basados en que la edad es mayor de 17 años
}
//el código aquí se ejecutará aunque no se cumpla la condición
````
En este caso declaramos la variable edad de tipo entero (int, ya que la edad no tiene decimales) y luego evaluamos si es mayor que el número 17, notemos que hacemos una comparación directa en la variable y un valor fijo utilizando el signo > y que la condición que se evalua se encuentra encerrada entre paréntesis.
Todo el código que agregemos dentro de las dos llaves ( { } ) se ejecutará si se cumple la condición solamente.

###Condiciones
Al final de cuentas toda condición que evaluamos en un bloque if termina siendo booleana, o sea que es verdadero o falso, algunos ejemplos.

````csharp
var edad = 17;
if(edad == 18){ //hacemos la comparación de igualdad con dos signos =
  //tiene exactamente 18 años de edad
}

if(edad > 18){
  //es mayor de 18, es decir el 18 no cumple la condición
}

if(edad >= 21){
  //la edad es igual o mayor a 21
}
````

Las condiciones de pueden combinar de muchas formas con operadores lógicos.
Exite otro tipo de condiciones que vamos a ver más adelante junto con otros operadores lógicos que podemos utilizar en las evaluaciones.

[Más sobre condiciones](condiciones.md)

##Repeticiones
Una repetición o iteración es una estructura que nos permite que algo ocurra un número de veces, por ejemplo que se muestre en la pantalla los números del 1 al 100, en lugar de escribir 100 veces la instrucción para imprimir en pantalla utilizamos una iteración.
La iteración más común es "for" y significar "hacer algo hasta cumplir con una condición" en general esa condición es un contador.

````csharp
for(int i = 1; i < 101; i++){
  //imprimir i
}
````

Esto es un poco más complicado, vamos por partes; dentro de los paréntesis hay tres datos escenciales:
- primero declaramos una variable del tipo int (para que la use "for" para contar) y le asignamos el valor 1.
- segundo una condición que hace que todo lo que está dentro de las llaves "{}" del "for" se repita hasta que esta condición se alcance, en este caso mientras i sea menos a 101
- y tercero "i++" para incrementar i en 1 cada vez.

Entonces este "bucle" (es el término correcto) for, se va a repetir 100 veces, ya que i comienza siendo 1, se incrementa una vez por cada repetición y tiene que hacerlo siempre que su valor sea menos a 101 (es decir, de 1 a 100).

[Más ejemplos con for](for.md)

Otra estructura de repetición muy usada es while, [Acá se puede ver su uso](while.md)

##Funciones o rutinas
Las funciones son una forma de agrupa código que persigue una funcionalidad para poder usarla varias veces, por ejemplo

````csharp
function void Saludar()
{
  //imprimir saludo
}
````

En este caso usamos la palabra clave "function" para indicar que queremos crear una función, y le ponemos un nombre (de momento ignoremos la palabra void, es necesaria pero la veremos en un instante)
Entonces, desde cualquier parte de nuestro código podemos utilizar la función:

````csharp
var edad = 38;

if(edad > 18)
{
  Saludar();
}
````
En este ejemplo si se da la condición "invocamos" la función, es decir, hacemos que se ejecute (los paréntesis son necesarios siempre en C#)
Como vemos todo lo que están entre las llaves ( { } ) es parte de la función (al igual que en caso del for y del if, las llaves definen los límites)
Veamos algunas algunas características de las funciones:
- Tienen un nombre único
- Puden recibir parámetros
- Tienen un valor de retorno

Vamos a explicarlo, ya vimos lo del nombre, si queremos llamar a una función unívocamente tiene que tener un nombre único, eso es claro.

###Parámetros en las funciones
¿Qué pasa si queremos que la función haga un cálculo dentro? tenemos que tener un modo de "pasarle" un valor a la función para que lo utilice, a estos valores (que pueden ser varios) se les llama "parámetros", veamos un ejemplo:

````csharp
function void CalcularEdad(int edad)
{
 if(edad < 18)
 {
  //no puede ver la película porque es menos
 }
}
````

Este código sería la "definición" de la función, básicamente recibe un parámetro (dentro de los paréntesis) al que llamamos "edad" que tiene un tipo int, luego, dentro de la función utilizamos la variable en nuestra comparación.
Para utilizar la función (es decir, invocarla) hacemos lo siguiente:

````csharp
var miEdad = 16;
CalcularEdad(miEdad);
````
En este caso declaramos la variable "miEdad" y luego llamamos a la función "CalcularEdad" y le pasamos esta variable como parámetro (podríamos pasar un valor diréctamente en lugar de una variable)

````csharp
CalcularEdad(16);
````

###Valores de retorno
Las funciones pueden "devolver" un valor, es decir, hacer una tarea (calcular un resultado) y devolverlo, por ejemplo:
````csharp
function int Doble(int valor) // function int indica que la función devuelve un valor del tipo int
{
  return valor * 2; //la palabra clave return indica que la función debe devolver el valor
}
````
En este ejemplo la función Doble, recibe un parámetro "valor" de tipo entero (int), la palabra void que usamos en los ejemplos anteriores se cambió por "int" para indicar que esta función devuelve un valor del tipo int (la palabra void que usábamos antes indica que no devuelve nada).
Simplemente recibe un parámetro entero y devuelve el doble ````return valor * 2````




