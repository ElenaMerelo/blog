---
layout: chapter
title: Guía de estilo
authors:
 - fdavidcl
category: meta
permalink: /styleguide/
---

Esta guía recoge algunos consejos sobre el estilo a seguir
a la hora de escribir un post, y además podrá servir de plantilla.

## Datos del post
Los datos del post son de la cajita que debe aparecer al principio
de cada publicación. No serán interpretados por el procesador
Markdown sino por Jekyll, para poder incrustar el post en la página
web correcta y añadir los datos necesarios:

    ---
    layout: chapter
    title: Guía de estilo
    authors:
     - fdavidcl
    category: meta
    ---

Algunas aclaraciones:

 * El `layout` debe ser siempre `chapter`. Existen otros layouts
 para otras páginas, pero no para los posts.
 * El título debe ser conciso y son preferibles los sustantivos a
 los verbos (por ejemplo, mejor "*Introducción a Javascript*" que
     "*Cómo programar en Javascript*" y que "*Una introducción a la
     programación en el lenguaje Javascript*"). No debe acabar en
     punto, aunque si tiene varias frases se pueden separar por
     puntos. Por ejemplo, "*Introducción a Javascript. Programación
     con prototipos*".
 * El autor es el identificador que hayáis añadido a `config.yml`.
 Si aún no tenéis un identificador, añadidlo.
 * En `category` solo puede haber una categoría. Debe ser más genérica
 que el tema que trate el post, pero no tanto como *informática*. Se
 pueden (y se deben) poner acentos.

También es un dato del post el nombre del archivo, que será del tipo
`2014-5-17-guia-de-estilo.md`. De él se extraerá la fecha y el enlace
permanente del post, así que no lo hagais largo (en general debe
    contener las palabras más importantes del título) y separad por
    guiones y no por mayúsculas. No introduzcáis símbolos ni acentos
    (números sí son válidos).

> **Nota**: Es importante que la codificación del archivo sea *UTF-8
> sin BOM*. Si escribís en Linux la codificación *UTF-8* bastará.

## Contenido del post

### El texto
Poco que decir aquí. No hace falta decir que cuidéis la ortografía y
la gramática :smile:. Si usáis un editor con vista previa de Markdown
(como [Atom](http://www.webupd8.org/2014/05/install-atom-text-editor-in-ubuntu-via-ppa.html),
o [StackEdit](https://stackedit.io/)) mejor que mejor, así no hay
problemas de formato tampoco.

Ah, no os paséis con el formato. Reservad la negrita para cosas muy
importantes, nunca resaltéis párrafos enteros.

### Títulos y secciones
Tenéis disponibles los títulos desde el nivel 2 (`##`) hasta nivel 6
(`######`). El nivel 1 se utiliza automáticamente para el título del
post. De nuevo, no escribáis un punto al final de un título. Evitad
utilizar cualquier otro tipo de separación entre apartados, no uséis
líneas horizontales (`* * *`) ni otro tipo de marcas. Si véis que la
estructura de los posts no es suficientemente visible, mandadme un
mensaje y mejoro el estilo de los títulos de sección.

### El código
Para escribir código tenemos dos sintaxis. o bien dejar 4 espacios de
margen, como el siguiente ejemplo

~~~markdown
    def codigo_en_ruby
      "Una prueba"
    end
~~~
que genera

    def codigo_en_ruby
      "Una prueba"
    end

o bien utilizar las marcas `~~~`, que además permiten especificar el
lenguaje:

~~~~markdown
~~~ruby
def codigo_en_ruby
  "Una prueba"
end
~~~
~~~~

que genera

~~~ruby
def codigo_en_ruby
  "Una prueba"
end
~~~

### Las matemáticas
Para incrustar ecuaciones en Latex, hay que hacerlo entre tildes
invertidas y dólares, dos dólares para las ecuaciones
en modo *display*. Ejemplos:

~~~markdown
`$E = mc^2$`
~~~

genera `$E = mc^2$`, y

~~~markdown
`$$ \sqrt[n]{x_1x_2 \dots x_n} \leq \frac{x_1+x_2+\dots+x_n}{n} $$`
~~~

`$$ \sqrt[n]{x_1x_2 \dots x_n} \leq \frac{x_1+x_2+\dots+x_n}{n} $$`

Las tildes invertidas nos evitan problemas con los caracteres de
formato de Markdown (como `_`, `*`, etc.).