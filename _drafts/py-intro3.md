---
layout: post
title:  "Introducción (continuación)"
permalink: /py-intro3/
show: true
---
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

# Listas
Al igual que los números y las cadena de carácteres, las listas son un tipo de dato en python. Una lista consiste en un sucesión de elementos (números, carácteres e incluso listas), separados por coma y encerrada por `[]`.

{% highlight python %}
  # Ejemplo de lista
  listaA = ['a', 'b', 'c', 1, 2, 3, True, False, '.1', '.2', '.3']
{% endhighlight %}

## Algunas características de listas
1. Pueden contener elementos de diferentes tipos.
2. A cada elemento le corresponde un índice.
3. Existen `métodos` para modificar las listas.

### Indexación
Tomando como ejemplo la lista construida previamente, a cada uno de sus elementos le corresponde un índice de acuerdo a su posición. Contando de izquierda a derecha, al primer elemento le corresponde el índice 0.

{% highlight python %}
  # Para mostrar el elemento de índice 0.
  listaA[0]
  # Para mostrar el elemento en la segunda posición
  listaA[1]
{% endhighlight %}

También se acepta contar de derecha a izquierda, en este caso, al primer elemento le corresponde el índice -1.

{% highlight python %}
  # Para mostrar el último elemento, o el primero, contando de derecha a izquierda.
  listaA[-1]
  # Para mostrar el anteúltimo elemento.
  listaA[-2]
{% endhighlight %}

**Es interesante hacer notar que a cada elemento de un `string` también le corresponde un índice.**

{% highlight python %}
  string = 'Rindfleischetikettierungsüberwachungsaufgabenübertragungsgesetz'
  # Primera letra
  string[0]
{% endhighlight %}

Por medio de los índices es posible modificar la lista (o string).

{% highlight python %}
  # Modificar el tercer elemento de la lista.
  listaA[2] = 'd'
{% endhighlight %}

Nos pueden interesar ciertos elementos.

{% highlight python %}
  # Todos los elementos desde la tercera posición.
  listaA[2:]
  # Todos los elementos desde la primera posición hasta la cuarta inclusive.
  # Cuarta posición: índice 3.
  # El elemento de índice 4 NO SE MUESTRA.
  listaA[:4]
  # Elemento con índices 1, 2, 3
  listaA[1:4]
{% endhighlight %}

### Métodos
Sólo diremos que los métodos son funciones especiales, definidas para trabajar con cierto tipo de objetos. [Aquí podrás encontrar una lista de métodos válidos para listas](https://docs.python.org/3/tutorial/datastructures.html){:target="_blank"}.

<a href='/py-condicionales/' style="float:right">Siguiente</a>
