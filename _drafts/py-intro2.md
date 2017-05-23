---
layout: post
title:  "Introducción (continuación)"
permalink: /py-intro2/
show: true
---
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

# Cadenas de carácteres o _strings_
Cuando se escribe un código, es común comentar para señalar algo importante. Si los comentarios toman una sola línea, basta con anteponer el símbolo `#`; caso contrario, el texto se encierra en `'''  '''`.

{% highlight python %}
  # Comentarios de una sola línea
  ''' Texto más largo, para describir una función o modelo.'''
{% endhighlight %}

Python puede también interpretar texto como un tipo de dato y por lo tanto operar con él. Los _strings_ se escriben entre comillas simples o dobles, como se muestra a continuación.

{% highlight python %}
  'a'  
  "b"
{% endhighlight %}

La importancia de este tipo de dato radica en que permite principalmente la interacción con el usuario, a partir de mensajes generados por medio de la función `print()`.

{% highlight python %}
  a = 1  
  b = 2
  c = 3 * a + b ** 2

  print('De acuerdo a los valores ingresados de a y b, c es igual a ', c)

{% endhighlight %}

## La función _print()_
Los siguientes ejemplos muestran diferentes formas de usar la función `print()`.

{% highlight python %}
a = 1.5
b = 3.8

c = a * b
print('El resultado de multiplicar a y b es ', c)
{% endhighlight %}

Es la forma quizá más sencilla de generar un mensaje. Antes de cerrar la comilla se deja un espacio, para que el valor de c esté separado del resto del texto.

{% highlight python %}
a = 1.5
b = 3.8

c = a * b
print('El resultado de multiplicar a y b es', round(c))
{% endhighlight %}

La función `round()` redondea el valor de c, por defecto al entero más próximo.

{% highlight python %}
j = 1e5
k = 13.28

l = j * k
print('El producto de j y k es', '%.3e'%l)
{% endhighlight %}

`'%.3e'%` afecta a la variable `l`, para que se muestre con notación científica. En este caso con 3 cifras decimales después de la coma.

{% highlight python %}
g = 8
h = 5

i = g/h
print(('Si dividimos {} por {}, el resultado es {}').format(g, h, i))
{% endhighlight %}

Otra forma de mostrar valores es usar el método `format()`, tal y como se muestra en el ejemplo.

## Asignación de variables
Otra forma de asignar variables es por medio de la función `input()`.

{% highlight python %}
  # El móvil se mueve con M.R.U.
  h0 = input('Ingrese el valor de la posición inicial en m: ')
  v = input('Ingrese el valor de la velocidad en m/s: ')
  t = input('Ingrese el valor del tiempo en s: ')

  r = h0 + v*t
  print('La distancia recorrida por el movil luego de un tiempo t es: ', r)
{% endhighlight %}

**Seguramente al ejecutar el código del bloque anterior obtendrás un mensaje de error.** Esto se debe a que el valor ingresado, si bien puede ser un número, es transformado por la función `input()` en un `string`. Esto se soluciona fácilmente, transformando un tipo de dato en otro:

{% highlight python %}
h0 = float(input('Ingrese el valor de la posición inicial en m: '))
v = float(input('Ingrese el valor de la velocidad en m/s: '))
t = float(input('Ingrese el valor del tiempo en s: '))

r = h0 + v*t
print('La distancia recorrida por el movil luego de un tiempo t es: ', r, 'm/s.')
{% endhighlight %}
