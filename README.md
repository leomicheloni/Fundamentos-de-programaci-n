# Fundamentos de programación

Éste es un pequeño resumen sobre conceptos de programación en el cual se han simplificado muchos conceptos para facilitar la comprensión y que el mismo sea más compacto.

##Qué es un programa?

Un programa es la forma en que le decimos a una computadora qué queremos que haga, paso a paso, con instrucciones simples, del mismo modo que cocinar es seguir una receta, un programa le dice a la computadora qué queremos que haga siguiendo un conjunto de pasos.

##Qué es un lenguaje de programación?

Las computadores no entienden nuestro lenguaje sino que utilizan algo conocido como "código máquina" (básicamente unos y ceros), un lenguaje de programación nos permite expresar aquello que queremos hacer de un modo comprensible por nosotros siguiendo ciertas reglas que luego es convertido a código máquina por un programa llamado "compilador". 
En este caso utilizaremos C# como lenguaje.

Desde un punto de vista práctico existen 3 elementos principales en la programación tradicional:

- Variables
- Decisiones, control de flujo
- Repeticiones

##Variables

Las variables son lugares en donde dejamos valores para utilizarlos después, por ejemplo, si queremos guardar un número de teléfono lo podemos dejar en una variable y luego recuperarlo.
````csharp
int telefono;         //reservamos un lugar en la memoria RAM de la computadora
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

En el ejemplo del teléfono simplemente guardamos el valor y ya, esto reserva un lugar en memoria para nuestra variable, pero también indicamos "int" cuando la asignamos por primera vez, esto es porque existen diferentes tipos de variables, es decir, no es lo mismo guardar un texto como "hola mundo" a guarda un número como "123123", nosotros tenemos que indicar a C# qué tipo de valor vamos a guardar en esa varible.
En el caso de C# los tipos más comunes son:

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

##Decisiones
Las decisiones son estructuras de control de flujo, es decir, permite decidir si hacer una cosa u otra dependiendo de ciertas circunstancia, por ejemplo podemos decir que alguien es mayor de edad basados en su edad. 
La estructura de control más utilizada es "if" se significar algo como "si se cumple cierta condición hacer esto", en el ejemplo de la edad sería así:

````csharp
int edad = 12;
if(edad > 17){
  //en esta parte hacemos algo basados en que la edad es mayor de 17 años
}
//el código aquí se ejecutará aunque no se cumpla la condición
````
En este ejemplo declaramos la variable edad de tipo entero (int, ya que la edad no tiene decimales) y luego evaluamos si es mayor que el número 17, notemos que hacemos una comparación directa en la variable y un valor fijo utilizando el signo >. Todo el código que agregemos dentro de las dos llaves ( { } ) se ejecutará si se cumple la condición.

