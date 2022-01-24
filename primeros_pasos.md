<!-- Título del capítulo -->
# Primeros pasos en Python.

Al iniciar el proceso de aprendizaje de cualquier lenguaje de programación, existe una actividad que puede ser considerada una tradición, ésta consiste en imprimir en pantalla el mensaje "Hola mundo", o "Hello World" en inglés. En aras de mantener la tradicion comenzaremos explorando las diferentes maneras que tenemos para mostrar información por pantalla. 

En Python existe una gran variedad de funciones que pueden ser utilizadas sin la necesidad de definirlas. La primera función que usaremos será `print()`. Esta función imprime en pantalla un mensaje, el mensaje puede ser un string o cualquier otro objeto. El objeto será transformado en un string antes de ser escrito en pantalla. 

Más adelante profundizaremos acerca de los tipos de datos como strings y objetos en Python, por ahora, para efectos prácticos, un string representa datos de tipo texto. Ahora bien, ya estamos listos para imprimir el mensaje de inicio, para ello escribimos la siguiente línea de código.

```python
print("Hello World")
```

<!-- Sección 1 -->
## Un hola mundo dinámico.

Finalmente hemos cumplido con la tradición, se ha mostrado un mensaje de "Hola Mundo" en nuestra pantalla. Ahora que hemos iniciado "formalmente" nuestro camino por el mundo de Python, en el resto del capítulo vamos a profundizar en otras formas de mostrar información en pantalla usando la función `print()`, pero primero, veamos otra función interesante que nos permitirá recibir información desde el exterior, la sintaxis de está función es:

```python
input("message")
```

La función `input()`, al igual que la función `print()`, se encuentra predefinida en el ambiente de Python, por lo que podemos usarla preocuparnos por su definición. El argumento que recibe la función es un `string` que se muestra en consola a modo de mensaje antes de introducir la entrada. Por último, esta función retorna un `string` que representa la entrada recibida por teclado. Esto es, cualquier información introducida antes de presionar la tecla `return`. Las siguientes líneas de código actualizan nuestro programa para escribir un saludo personalizado.

```python
print("Hello world")
name = input("Introduce your name: ")
print("Hello ", name)
```

Después de imprimir el mensaje "Hello world" el programa tiene dos líneas adicionales. El código anterior genera la siguiente salida.

```bash
Hello world
Introduce your name: John
Hello John
```

Las dos sentencias adicionales en nuestro programa realiza varias cosas, vamos a explicar cada una de ellas por separado.

```python
name = input("Introduce your name: ")
```

La sentencia anterior, como se mencionó anteriormente, utiliza una función predefinida `input(message)` que muestra un mensaje en forma de string justo antes de introducir información por teclado. Luego de presionar la tecla `return` la función devuelve el mensaje escrito por teclado para ser almacenado en la variable `name`.

## Variables en Python

Debido a su importancia, es necesario explicar formalmente el concepto de variable en programación

Las variables en cualquier lenguaje de programación sirven como punteros a espacios en la memoria del computador donde podemos almacenar información, a esta información se le conoce también como datos, estos datos pueden ser strings, números, booleanos (verdadero y falso) etc. Además, también podemos almacenar estructuras de datos. Todo esto será detallado en los capítulos siguientes.

<div style="background-color:red">
    <h3>Hacer gráfico que represente el concepto de variable</h3>
</div>

Al tener un puntero hacía el espacio en memoria en el que se encuentra un dato en particular, podemos acceder a esta información en otras líneas de código de forma conveniente. Basta sólo con usar el nombre de la variable para acceder al dato al que está hace referencia, en el ejemplo anterior, el nombre de la variable es `name`

```python
print("Hello ", name)
```

Finalmente, la sentencia anterior recibe dos argumentos, esto es porque la función `print()` puede recibir un número variable de argumentos, todos separados por coma. En este caso, recibe el mensaje "Hello ", y la variable name que permitirá acceder a la información a la cual esta variable apunta.

## ¿Por qué el nombre de variable?

Quizás en estos momentos te preguntes la razón del nombre variable, esto es porque la información a la que estas variables apuntan pueden variar a lo largo de la ejecución de un programa. Por ejemplo, veamos el siguiente programa:

```python
age = input("Escribe tu edad: ")
print("Tu edad es: ",age)
age = 100
print("Tu edad es: ",age)
age = "Esto debería ser un número"
print("Tu edad es: ",age)
```

En el programa anterior el dato al que hace referencia la variable `age` cambia en tres oportunidades, la primera vez se almacena la edad introducida con la función `input()` Luego esta se establece en 100 y finalmente almacena un string. 

## Tipado dinámico.

A diferencia de otros lenguajes de programación, una de las características de Python, es que se trata de un lenguaje de tipado dinámico, esto quiere decir, que no necesitamos definir el tipo de dato que la variable hace referencia, en el ejemplo anterior, el dato al que hace referencia la variable `age` no sólo cambia de valor, si no que además cambia de tipo, ya que la primera vez que la variable `age` es usada, recibe la salida de la función `input()` que será un string incluso si el dato introducido es un número, luego, la `age` almacena el número 100, para terminar con un nuevo string.

Para observar esto con más claridad, vamos a usar la función predefinida `type()` esta función indica el tipo de dato de la variable que se pasa como argumento, modifiquemos un poco el programa anterior para observar el cambio en el tipo de dato.

```python
age = input("Escribe tu edad: ")
type(age)
age = 100
type(age)
age = "Esto debería ser un número"
type(age)
```
Para mayor claridad, se elimina la función `print()`, de tal forma que sólo observaremos la variación del tipo de dato.

```python
<class 'str'>
<class 'int'>
<class 'str'>
```

Por ahora concentremos en la parte donde se indica el tipo de dato, y olvidemos por un momento la palabra reservada `class` que básicamente nos indica que estamos manipulando objetos, esto se trata con más detalle en el capítulo correspondiente a clases y objetos. Vemos que durante la ejecución del programa el tipo de dato al que hace referencia la variable `age` cambia tanto de valor como de tipo. 

El tipado dinámico puede ser una ventaja, ya que nos brinda mayor flexibilidad a la hora de escribir código, sin embargo, es importante destacar que esta podría ser una fuente considerable de errores, por lo que se debe tener claridad acerca del tipo de dato que manejarán las variables a la hora de escribir código Python.

## Convenciones para escribir variables.

Cada lenguaje de programación tiene su caracterísitcas propias que lo diferencian de otros lenguajes, estas diferencias pueden ser inherentes a la forma en la que dicho lenguaje está definido, otras características se han establecido no por las restricciones del lenguaje si no por conveniencia, y en muchas ocasiones por estilo. Veamos algunas de los estilos más populares que podemos encontrar para escribir el nombre de las variables.

### Camel Case

Usando este estilo, las palabras no se separan con espacios o signos de puntuación, en su lugar, la separación de las palabras se hace escribiendo la primera letra en mayúscula, por ejemplo:

```
programmingIsEasy
```

La variación con la primera letra en mayúscula también es aceptada.

```
ProgrammingIsEasy
```
<div style="background-color:red">
    <h3>Mencionar el origen del nombre Camel Case</h3>
</div>


### Snake Case

Si hacemos uso del estilo `snake case`, en este caso las palabras se separan por un guión bajo ( _ ) en lugar del espacio. El ejemplo anterior con el estilo `snake case` quedaría de la siguiente forma.

```
programming_is_easy
```

Ahora bien, en este libro estamos interesados en Python, así que haremos uso de las convenciones establecidas para escribir código haciendo uso de este lenguaje de programación. Para escribir variables en Python debemos hacer uso del estilo `snake case`, específicamente podemos nombrar algunas reglas que se deben tomar en cuenta a la hora de escribir nombres de variables en Python.

* Debe ser todo en minúscula
* Además, el nombre debe ser descriptivo, es decir, evitar nombres como a, b, o x para variables. En este sentido, lo que se busca es tener una idea de lo que representa la variable con sólo leer el nombre.
* Si el nombre de la variable está formado por más de una palabra, estas deben ir separadas por un guión bajo, haciendo uso del estilo `snake case`.

El último punto es importante ya que en Python, así como en la mayoría de los lenguajes de programación, el espacio es usdado como separador, o para indicar que algo ha terminado. Por ejemplo, si intentamos declarar una variable de la siguiente forma:

```python
last name = "my last name"
```

Python arrojará un error de sintaxis, pues no cumple con las especificaciones del lenguaje para declarar una variable.

Un aspecto importante de las convenciones es que se crearon para facilitar la lectura y escritura de código, de tal forma que la lectura del código de forma fluida y coherente, pero en muchos casos no tiene nada que ver con el comportamiento del lenguaje. Veamos por ejemplo, el siguiente programa.

```python
a = 3
b = 4
c = 0.5 * a * b

print(c)
```
El código anterior describe una serie de operaciones aritméticas, que no representan mayor problema para seguir, sin embargo, es difícil determinar la naturaleza de la operación, hasta ahora son sólo operaciones sin ningún significado aparente, ahora veamos el mismo código escrito haciendo uso de las convenciones descritas anteriormente.

```python
base = 3
altura = 4
area_triangulo = 0.5 * base * altura 
print(area_triangulo)
```

En este caso, para la mayoría de los lectores será evidente que trata de hacer el las líneas de códigos anteriormente. Se trata simplemente del cálculo del área de un triángulo. Este ejemplo es en extremo sencillo, sin embargo, estoy seguro que para la mayoría la segunda forma facilita la interpretación del código, ahora imaginemos que los cálculos que se intentan hacer son más complejos, imaginen como será de complicado para el programador que escribe el código o cualquier otro que tenga acceso al código, leer ecuaciones o problemas más complejos con variables nombradas como a, b, c, x, y, c, etc.

Por último, Python no tendría problemas en identificar una variable nombrada usando el estilo `camel case`, por ejemplo:

```python
lastName = "my last name"
```
La línea anterior creará exitosamente una variable llamada `lastName`, sin embargo, el estilo utilizado para crearla no será el correcto, por lo que se estará incurriendo en una mala práctica de escritura de código en Python.


## Sentencias en Python

## Ejercicios


