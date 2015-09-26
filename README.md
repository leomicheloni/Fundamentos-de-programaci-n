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
var telefono = 123123123;
````
Algunas cosas más sobre variables:
- Tienen un nombre único que las identifica (dentro del contexto en que están)
- La acción de "guardar" un valor dentro a una variable se conoce como "asignación"

En el ejemplo anterior asignamos el valor 123123123 a la variable "telefono", a partir de ahora podemos recuperar ese valor en otra parte de nuestro programa y, por supuesto, podemos cambiarlo cuando queramos.

````csharp
telefono = 011123123123;
`````

En este ejemplo cambiamos el valor de la variable "telefono", nótese que ya no usamos la palabra "var" delante, la misma sólo se utiliza al momento de declarar la variable.

## Tipos de variables


