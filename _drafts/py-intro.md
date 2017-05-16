---
layout: post
title:  "Introducción"
permalink: /py-intro1/
show: true
---
# Operaciones aritméticas
Python nos permite realizar las operaciones más comúnes: suma, resta, multiplicación, división y potenciación.

{% highlight python %}
1 + 2 # Suma
1 - 2 # Resta
1 * 2 # Multiplicación
1 / 2 # División
1 ** 2 # Potenciación
{% endhighlight %}

Otras operaciones son:

{% highlight python %}
1 // 2 # Calcula la parte entera del cociente
1 % 2 # Calcula el resto del cociente
{% endhighlight %}

Si se quiere hacer cálculos sucesivos, es posible almacenar los resultados asignándolos a una variable:

{% highlight python %}
a = 1 + 10 * (1 + 2) - 0.1 ** 2
b = 3 * a
{% endhighlight %}

La forma de asignar variables mostrada en el bloque anterior es especialmente útil cuando se trabaja con constantes.

# Tipos de números
Como veremos más adelante, python soporta diferentes tipos de datos; uno de ellos son los números, pero no todos los números son iguales. Estos pueden ser:

- Enteros (integer)
- Decimales (float)
- Complejos (complex)


Para conocer de qué tipo de dato se trata, python nos ofrece la función `type()`, cuyo uso se ilustra en el próximo ejemplo.

{% highlight python %}
a = 1 # Entero
b = 1.0 # Decimal
c = 1 + 2j # Complejo

type(a)
{% endhighlight %}

**¿Qué ocurre si operamos con diferentes tipos de datos?** El resultado adopta el tipo de dato con mayor información.

# Otras operaciones

Para llevar adelante otro tipos de cálculos, la forma más sencilla es **importar una librería**. Si sólo se trabaja con números reales conviene importar la librería _math_. Esta librería ofrece funciones y constantes para realizar los cálculos.

{% highlight python %}
from math import *
dir(math) # Muestra un directorio de funciones y constantes
{% endhighlight %}

La primera línea del ejemplo anterior importa todos los elementos de la librería al espacio de trabajo. Existen otras formas de importar, pero por simplicidad se mostró sólo una, pese a que no es la mejor.

{% highlight python %}
log(10) # Calcula el logaritmo natural de 10
e**2 # Calcula el cuadrado del número e
{% endhighlight%}

Si se trabaja con números complejos, la librería _cmath_ ofrece funciones adicionales.

**Es altamente recomendable acostumbrarse a leer la documentación de las librerías para conocer un poco mejor qué nos ofrecen y cómo usarlas**. A continuación, enlaces para las documentaciones de las librerías usadas en esta sección.

- [math](https://docs.python.org/2/library/math.html)
- [cmath](https://docs.python.org/2/library/cmath.html)


<a href='/py-intro2/' style="float:right">Siguiente</a>
