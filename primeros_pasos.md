<!-- Título del capítulo -->
# Primeros pasos en Python.

Al iniciar el proceso de aprendizaje de cualquier lenguaje de programación, existe una actividad que puede ser considerada una tradición, ésta consiste en imprimir en pantalla el mensaje "Hola mundo", o "Hello World" en inglés. En aras de mantener la tradicion comenzaremos explorando las diferentes maneras que tenemos para mostrar información por pantalla. 

En Python existe una gran variedad de funciones que pueden ser utilizadas sin la necesidad de definirlas. La primera función que usaremos será la función `print()`. Esta función imprime en pantalla un mensaje, el mensaje puede ser un string o cualquier otro objeto. El objeto será transformado en un string antes de ser escrito en pantalla. 

Más adelante profundizaremos acerca de los tipos de datos como strings y objetos en Python, por ahora, para efectos prácticos, un string representa datos de tipo texto. Ahora bien, ya estamos listos para imprimir el mensaje de inicio, para ello escribimos la siguiente línea de código.

```python
print("Hello World")
```

<!-- Sección 1 -->
## Dando formato a las cadenas en Python.

Finalmente hemos cumplido con la tradición, hemos mostrado un mensaje de "Hola Mundo" en nuestra pantalla. Ahora que hemos iniciado "formalmente" nuestro camino por el mundo de Python, en el resto del capítulo vamos a profundizar en otras formas de mostrar información en pantalla usando la función `print()`, pero primero, veamos otra función interesante que nos permitirá recibir información desde el exterior, la sintaxis de está función es:

```python
input("message")
```

La función `input()` al igual que la función `print()` se encuentra predefinida en el ambiente de Python, por lo que podemos usarla sin problemas. El argumento que recibe la función es un `string` que se muestra en consola a modo de mensaje antes de introducir la entrada. Además, esta función retorna un `string` que representa la entrada recibida por teclado. Esto es, cualquier cantidad de información introducida antes de presionar la tecla `return`

 