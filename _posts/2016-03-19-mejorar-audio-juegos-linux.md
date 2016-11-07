---
title: Cómo activar la escucha binaural en Linux
tags: [Audio]
categories: [Linux]
published: yes
---
El otro día, buscando ciertas configuraciones de Pulseaudio en la wiki de Arch Linux, encontré un apartado que decía **"*Binaural Audio with OpenAL*"**. Investigué y resulta que es para que si tienes auriculares estéreo y ejecutas un juego o programa que use **OpenAL** (por ejemplo, Minecraft) lo que pase a la izquierda suene por el auricular izquierdo y lo que pase a la derecha suene por el derecho. Y creedme, la mejora se nota una barbaridad.

Para activarlo, sólo hay que ejecutar esto en la terminal:
{% highlight bash %}
echo "hrtf = true" >> ~/.alsoftrc
{% endhighlight %}
Para el que no lo entienda, este comando crea el archivo "*.alsoftrc*" en tu carpeta de usuario y escribe en él "*hrtf = true*". Si no os gusta la mejora, con eliminar ese archivo basta.

[Aquí][ArchWiki] tenéis el artículo de la wiki (en inglés).


[ArchWiki]: https://wiki.archlinux.org/index.php/Gaming#Binaural_Audio_with_OpenAL
