---
layout: page
title: Talleres
permalink: /talleres/
---
A continuación te presentamos la lista de cursos organizados por la comisión.
Para conocer los detalles, no dudes en hacer clic en las opciones que más te gusten.

<ul>
  {% for post in site.posts %}
    {% if post.show %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
