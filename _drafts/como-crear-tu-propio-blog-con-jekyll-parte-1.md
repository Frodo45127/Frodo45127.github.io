---
layout: post
title: Cómo crear un blog con Jekyll (parte 1)
tags: [tutoriales, jekyll, blogs, github]
categories: [tutoriales, jekyll, github]
published: no
---
Siempre me ha gustado aprender a hacer las cosas. Si me decían que hiciera algo que no sabía hacer, prefería intentar aprender a hacerlo yo por mi cuenta en lugar de preguntar "¿Cómo se hace?". Y eso con el tiempo no ha cambiado. Pero eso no sirve para todo, así que por eso voy a hacer esta serie de tutoriales.

- [ ]

El objetivo de estos tutoriales será **aprender a montar nuestro propio blog con Jekyll en GitHub**. Como probablemente os daréis cuenta, este blog está a medias. Eso es porque lo voy haciendo "*sobre la marcha*", y del resultado de esos esfuerzos van saliendo estos tutoriales. Pero bueno, no me gusta hacer esperar a la gente, así que al lío.

Primero, este tutorial no es para gente sin conocimientos básicos de la web. Y con esto me refiero a que, si sigues leyendo, daré por hecho que posees conocimientos básicos de:

1. HTML.
2. CSS.
3. Markdown (esto se aprende en 10 minutos).
4. Inglés (parte de la documentación está en el idioma de Shakespeare).

Si careces de conocimientos sobre alguno de los temas de la lista pero quieres continuar leyendo, al final del post hay documentación y páginas que te serán útiles.

Segundo, debemos tener claros varios conceptos:

- **Qué es una *página web dinámica***: una página web dinámica es una página cuyo contenido **se genera automáticamente cuando el usuario entra a la página**. Por ejemplo, la página principal de un blog de blogger carga los 5 últimos posts publicados desde una base de datos y muestra una versión reducida cada vez que un usuario entra. Así, cuando el autor publica un nuevo post, el contenido de la página principal cambia. Pueden hacer muchas cosas, pero tardan mucho más que una página estática en cargar.
- **Qué es una *página web estática***: una página web estática es una página cuyo contenido **no cambia a menos que una persona lo cambie**. Por ejemplo, la página ```Acerca de``` de este mismo blog. No pueden cargar contenido *dinámicamente*, pero son muy rápidas cargando.
- **Qué es *Jekyll***: Jekyll es un generador de páginas estáticas. Lo que hace es generar un sitio web estático (con todas sus páginas) cada vez que modificas algo. De manera que tienes una web estática que se comporta como si fuera una web dinámica. Esto combina la posibilidad de tener "*contenido dinámico*" con la velocidad de carga de una web estática.
- **Qué es *GitHub***: GitHub es una plataforma para alojar proyectos de código abierto. En nuestro caso la usaremos porque permite que te montes tu propio sitio web y porque trabaja con Jekyll integrado.

### Enlaces de ayuda y documentación

- [Documentación de HTML][html-mozilla-doc].
- [Documentación de CSS][css-mozilla-doc].
- [Documentación de Markdown][markdown-doc].
- [Documentación del "GitHub Flavored Markdown"][markdown-github-doc] (está en inglés).
- [Documentación de Jekyll][jekyll-website] (está en inglés).
- Podéis aprender más sobre las páginas web dinámicas en [este enlace][web-dinamica] (está en inglés).
- Podéis aprender más sobre las páginas web estáticas en [este enlace][web-estatica] (está en inglés).

[web-dinamica]: https://en.wikipedia.org/wiki/Dynamic_web_page
[web-estatica]: https://en.wikipedia.org/wiki/Static_web_page
[jekyll-website]: http://jekyllrb.com/
[html-mozilla-doc]: https://developer.mozilla.org/es/docs/Web/HTML
[css-mozilla-doc]: https://developer.mozilla.org/es/docs/Web/CSS
[markdown-doc]: http://joedicastro.com/pages/markdown.html
[markdown-github-doc]: https://help.github.com/articles/github-flavored-markdown/

*[HTML]: Hyper Text Markup Language
*[CSS]: Cascading Style Sheets
