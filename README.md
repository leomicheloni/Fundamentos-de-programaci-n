# Fundamentos de programación

##Qué es un programa?

Un programa es la forma en que le decimos a una computadora qué queremos que haga, paso a paso, con instrucciones simples, del mismo modo que cocinar es seguir una receta, un programa le dice a la computadora qué queremos que haga siguiendo un conjunto de pasos

Desde un punto de vista práctico existen 3 elementos principales en la programación

- Variables
- Decisiones
- Repeticiones

##Variables

Las variables son lugares en donde dejamos valores para utilizarlos después, por ejemplo, si queremos guardar un número de teléfono lo podemos dejar en una variable y luego recuperarlo.
````csharp
int telefono = 123123123;
````
Algunas cosas más sobre variables:
- Tienen un nombre único que las identifica (dentro del contexto en que están)
- La acción de "guardar" un valor dentro a una variable se conoce como "asignación"

En el ejemplo anterior asignamos el valor 123123123 a la variable "telefono", a partir de ahora podemos recuperar ese valor en otra parte de nuestro programa y, por supuesto, podemos cambiarlo cuando queramos.

````csharp
telefono = 011123123123;
`````

En este ejemplo cambiamos el valor de la variable "telefono", nótese que ya no usamos la palabra "int" delante, la misma sólo se utiliza al momento de declarar la variable.

## Tipos de variables

En el ejemplo del teléfono simplemente guardamos el valor y ya, esto reserva un lugar en memoria para nuestra variable, pero también indicamos "int" cuando la asignamos por primera vez, esto es porque existen diferentes tipos de variables, es decir, no es lo mismo guardar un texto como "hola mundo" a guarda un número como "123123123", nosotros tenemos que indicar a C# qué tipo de valor vamos a guardar en esa varible.
En el caso de C# los tipos más comunes son:

- Enteros: int
- Cadenas de texto: string
- Números con punto flotantes (decimales): double
- Booleanos (true o false): bool

Existen otros tipos pero por ahora vamos a utilizar estos.

