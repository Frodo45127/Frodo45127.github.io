---
layout: post
title: Cómo importar tu blog de Blogger a Jekyll sin morir en el intento
tags: [Jekyll, Blog, Blogger]
categories: [jekyll]
published: yes
---
Yo tuve un blog en Blogger, o Blogspot, y el ótro día se me ocurrió la no tan genial idea de "***Oye, ¿y si importo algunas de las entradas del blog viejo al nuevo?***". Si alguna vez vuelvo a pensar en algo así, pegadme un tiro.

Para que no tardéis un día entero en hacerlo como tardé yo, os ahorraré muchos problemas: **ignorad la documentación de Jekyll**. Está muy desactualizada y no funciona. Y sí, tarde una hora en darme cuenta.

Buscando **encontré [un Gist][Blogger-to-Jekyll-original] para esto mismo** pero, ¿qué pasaba?. No convertía a Markdown las entradas, y como tuvieran un `:` en algún lado del título o de las tags, esa entrada ni la convertía. Es más, con dos `:` en una misma entrada dejaba de funcionar. Así que, sin tener ni puñetera idea de Ruby, **le hice un fork al Gist y lo apañé**. Ahora traga con todo, pero os aconsejo revisar los nuevos post antes de publicarlos, porque a veces no va del todo fino. [Aquí][Blogger-to-Jekyll-modificado] os lo dejo.

En la documentación del Gist (ese trozito de texto al principio que nadie lee) pone cómo usarlo, ***y los requisitos que necesita***. Ale, que lo disfrutéis.

[Blogger-to-Jekyll-original]: https://gist.github.com/kennym/1115810
[Blogger-to-Jekyll-modificado]: https://gist.github.com/Frodo45127/600043b73956ec9e5faf
