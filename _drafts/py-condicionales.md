---
layout: post
title:  "Condicionales y bucles"
permalink: /py-condicionales/
show: true
---
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

# Operaciones de comparación
Los operadores de comparación en python son: `<, >, <=, >=, ==, !=`. Estas operaciones son muy útiles para definir condiciones, como veremos más adelante.

Como operaciones, pueden arrojar dos posibles resultados: `True` o `False`. Podemos probar escribiendo los siguiente ejemplos en la consola.

{% highlight python %}
  2 == 2 # Igual
  2 != 2 # Distinto
  2 < 1 # Menor que
  2 <= 1 # Menor o igual que
{% endhighlight %}

**True y False son `booleanos`, un tipo de variable. También le corresponden los valores 1 y 0, respectivamente.**

Las comparaciones se pueden ver afectadas por otros operadores como: `and, or, not`.

{% highlight python %}
  not 2 < 1 # Quiere decir lo contrario de la proposición escrita.

  2 > 1 and 4 < 6 # Será cierto sólo si ambas proposiciones son verdaderas.

  2 > 1 OR 4 > 6 # Será cierto si al menos una de las proposiciones son verdaderas.
{% endhighlight %}

# Condicionales
Por medio de condicionales es posible escribir un programa que se adapte a diferentes situaciones. Un ejemplo sencillo es el siguiente:

**Dada una lista de elementos arbitrarios, se quiere saber si el elemento `'e'` pertenece o no a la lista ingresada. Cualquiera sea el caso, se deberá imprimir un mensaje que informe debidamente al usuario.**

{% highlight python %}
lista = ['a', 'b', 'c', 'f']

if 'e' not in lista:
  print("'e' no es un elemento de la lista.")
else:
  print("'e' pertenece a la lista.")
{% endhighlight %}

Hay varios puntos por aclarar:
1. Las líneas con las condiciones comienzan con: `if, elif,` o `else`, y terminan siempre con `:`. `if` es la primera condición, `elif` se ocupa para las siguientes condiciones y `else` para todos los casos restantes, si los hubiere.
2. La siguiente línea, después de los `:`, indica la acción a realizar en caso de que la condición se cumpla. Algo muy importante es respetar la `identación`, es decir, dejar cuatro espacios antes de escribir.

# Bucles
Sirven para automatizar ciertas operaciones e iterar.
## Bucles con `for`

Se utiliza para llevar a cabo una operación para cada uno de los elementos de un conjunto. En el siguiente ejemplo, se generan 10 valores enteros (de 0 a 9) por medio de la función `range()`. Para cada uno de esos elementos, se calcula su cuadrado y se almacena su valor en la variable x. En el siguiente paso se agrega el valor de x a la lista y luego de terminado el bucle se la imprime.

{% highlight python %}
  # Lista vacía
  lista2 = []

  for i in range(10):
    x = i ** 2
    lista2.append(x)

  print(lista2)
{% endhighlight %}

**La diferencia entre imprimir la lista completa luego de acabado el bucle o imprimir cada vez que se agrega un valor depende de la identación. En el ejemplo, al no dejar los cuatro espacios, python interpreta que esa sentencia no es parte del bucle y la ejecuta por tanto luego de que este ha terminado.**

## Bucles con `while`

Sirven para llevar a cabo operaciones repetidamente, mientras se siga cumpliendo cierta condición. En el siguiente ejemplo, se agregan valores a una lista mientras su cantidad de elementos sea menor a 10. Los valores a agregar empiezan en 0 y aumentan en una unidad.

{% highlight python %}
lista3 = []
i = 0
while len(lista3) < 10:
    lista3.append(i)
    i +=1
print(lista3)
{% endhighlight %}

<a href='/py-funciones/' style="float:right">Siguiente</a>
