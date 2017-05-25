---
layout: post
title:  "Funciones"
permalink: /py-funciones/
show: true
---
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

# Funciones

Hasta aquí hemos visto muchas funciones definidas por python, [para ver la lista completa has click aquí](https://docs.python.org/3/library/functions.html). Ahora veremos como definir nuestras propias funciones.

{% highlight python %}
def func(x, y):
  return x * y
{% endhighlight %}

1. Al igual que con los condicionales y bucles, aquí también hay un término específico: `def`.
2. El nombre de la función es arbitrario y entre `()` se indican las variables. Los `:` al final de la sentencia no pueden faltar.
3. Luego de los `:`, las líneas siguientes deben respetar la identación.
4. El término `return` indica que la función devuelve un valor. Este valor puede ser luego asignado a una variable y ser usado en cálculos futuros. Si no quisiéramos usar el valor que devuelve la función, sino simplemente verlo, alcanzaría con escribir `print(x * y)`.
5. Cualquier comando después de la línea con `return` no formará parte de la definición de la función.

## Funciones y condicionales
Empecemos corriendo el siguiente programa y veamos lo que ocurre.

{% highlight python %}

def mov_cal(r0, v0, a, t):
    '''
    Esta función calcula el desplazamiento  y la velocidad de un móvil que se mueve con Movimiento Rectilíneo Uniforme o Movimiento Rectilíneo Uniformemente Variado.
    '''
    if mov == 'mru':
        a = r0 + v0 * t
        b = v0
        return r, v
    elif mov == 'mruv':
        a = r0 + v0 * t + 0.5 * a * t ** 2
        b = v0 + a * t
        return a, b

mov = input('¿El móvil se mueve con MRU o MRUV? ')
mov = mov.lower()
if mov == 'mru':
    r0 = float(input('Posición inicial: '))
    v0 = float(input('Velocidad inicial: '))
    a = 0
    t = float(input('Tiempo: '))
    r, v = mov_cal(r0, v0, a, t)
    print(('El movil ha recorrido {} m en {} s, alcanzando una velocidad final de {}.').format(r, t, v))
elif mov == 'mruv':
    r0 = float(input('Posición inicial: '))
    v0 = float(input('Velocidad inicial: '))
    a = float(input('Aceleración: '))
    t = float(input('Tiempo: '))
    r, v = mov_cal(r0, v0, a, t)
    print(('El móvil con una aceleración constante de {} m2/s, se desplaza {} m en {} s y alcanza una velocidad final de {} m/s').format(a, t, r, v))
else:
    raise ValueError('No se acepta este tipo de movimiento.')

{% endhighlight %}

1. El programa nos pregunta que tipo de movimiento tiene el móvil. A continuación pide que ingresemos los valores de posición y velocidad iniciales, junto con el tiempo transcurrido. Sólo si el móvil se mueve con MRUV, el programa pide que se ingrese un valor de aceleración. Al final arroja un mensaje con los valores calculados de desplazamiento y velocidad final.
  - Analizando el programa, se observa el uso de condicionales. El usuario ingresa el tipo de movimiento y a partir de esto, el programa puede seguir diferentes caminos, dependiendo de la condición que se cumpla.
  - La variable `mov` se ve modificada por el método `lower()`, que transforma a minúscula las letras. Entonces, no importa que el usuario escriba MRU o mru, el programa lo transforma a mru y continúa con los pasos siguientes.
  - Los datos ingresados no se pueden utilizar de inmediato en cálculos porque son strings. La función `float()` los transforma en números.
2. Una vez ingresados los datos, se usa la función `mov_cal` definida antes en el programa.
  - La función también usa condicionales para usar diferentes ecuaciones, de acuerdo al tipo de movimiento.
  - La función tiene cuatro argumentos: `r0, v0, a, t` y devuelve `a, b`.
  - La línea `r, v = mov_cal(r0, v0, a, t)` es lo mismo que llamar _y_ al valor de f(x=5). La función calcula dos valores, la posición y la velocidad finales, y los asigna a las variables r y v.
3. Si se ingresa algo distinto de MRU o MRUV, el programa muestra un mensaje de error. Esto se puede hacer usando la expresión `raise ValueError('mensaje')`.

## Funciones y Bucles
La siguiete función inspecciona cada elemento de una lista y muestra el mayor de ellos.
{% highlight python %}

def mimax(xs):
    ''' Encuentra el mayor valor de una lista. '''
    inicio = 0
    for i in xs:
        if i > inicio:
            inicio = i
    print(i)

{% endhighlight %}

<a href='/py-matplotlib/' style="float:right">Siguiente</a>
