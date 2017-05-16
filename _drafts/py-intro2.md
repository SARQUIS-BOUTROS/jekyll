---
layout: post
title:  "Introducción (Continuación)"
permalink: /py-intro2/
show: true
---
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

# Tipos de datos
En la sección anterior se dijo que python soporta diferentes tipos de datos. En esta sección describiremos brevemente a algunos de ellos.

## Cadenas de carácteres o _strings_
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

El uso más común de los _strings_ radica en generar mensajes para el usuario, por medio de la función `print()`.

{% highlight python %}
  a = 1  
  b = 2
  c = 3 * a + b ** 2

  print('De acuerdo a los valores ingresados de a y b, c es igual a ', c)

{% endhighlight %}

Cada elemento de un _string_ tiene un índice que va de de cero en adelante, contando de izquierda a derecha.

{% highlight python %}
  palabra = 'Rindfleischetikettierungsüberwachungsaufgabenübertragungsgesetz'
  len(palabra) # Cuenta la cantidad de elementos
{% endhighlight %}

La palabra tiene 63 caracteres. A la primera letra le corresponde el índice 0, a la última el índice 62

{% highlight python %}
  palabra[0] # Muetra el elemento en la posición 0
  palabra[0:4] # Muestra los elementos en las posiciones 0, 1, 2 y 3
  palabra[:4] # Muestra los elementos en las posiciones 0, 1, 2 y 3
  palabra[4:] # Muestra los elementos con índice 4 en adelante
{% endhighlight %}

Lo que acabamos de hacer para trivial, pero en realidad resulta muy importante, especialmente cuando se trabaja con listas. Los intervalos son abiertos a la derecha, es decir, el elemento de índice 4 no aparece en el resultado de las segunda y tercera líneas.

Podemos modificar la palabra:

{% highlight python %}
  palabra[0] = 'r'
  palabra
{% endhighlight %}

# Listas

Las listas consisten en una sucesión de elementos separados por coma y encerrada en corchetes; bastante parecidas a los strings; puesto que podríamos haber dicho que eran una sucesión de elementos (caracteres letras o números) encerrados en comillas.

{% highlight python %}
  alumnos = ['Ana', 'Bruno', 'Carla', 'Otros']
  type(alumnos)
{% endhighlight %}

Al igual que con los strings, los elementos de una lista tienen asociado un índice.

{% highlight python %}
  alumnos[0] # Arroja el primer elemento de la lista
{% endhighlight %}

Las listas son objetos con métodos muy útiles, detallados [aquí](https://docs.python.org/3/tutorial/datastructures.html). Un método comúnmente utilizado es `append()`, el cual agrega un elemento nuevo a una lista.

{% highlight python%}
  alumnos.append('Nuevo') # Agrega el elemento al final de la lista
  alumnos.insert(3, 'Diego') # Agrega el elemento en la posición de índice 3
{% endhighlight %}

# Tuplas
Son también sucesiones de elementos separados por coma, encerrados en paréntesis o solos.

{% highlight python %}
alumnos = ('Ana', 'Bruno', 'Carla', 'Otros')
alumnos = 'Ana', 'Bruno', 'Carla', 'Otros' # También es válido obviar los ()
{% endhighlight %}

A diferencia de las listas, una tupla no es un objeto que pueda actualizarse en etapas posteriores.

# Diccionarios
Son sucesiones de elementos separados por coma y encerrados entre llaves, que se diferencian con las listas y tuplas en que sus elementos son pares `key:value`. Supongamos que a cada elemento de la lista alumnos le corresponde un ID numérico.

{% highlight python %}
  dict = {'Ana':1, 'Bruno':2, 'Carla':3, 'Otros':4}
{% endhighlight %}

  
