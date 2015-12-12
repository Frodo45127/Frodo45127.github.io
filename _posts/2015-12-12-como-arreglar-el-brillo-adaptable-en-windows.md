---
layout: post
title: Cómo desactivar el brillo adaptable en un portátil con Windows
tags: [tutoriales, tips, brillo adaptable]
categories: [tutoriales, tips]
published: yes
---
Tengo un portátil HP. Es una basura, pero es lo que tengo. Y desde que tenía Windows 8 tiene la puñetera manía de cambiarme el brillo de la pantalla cuando le da la gana. Tras buscar un poco, descubrí que el culpable era el **brillo adaptable**. Esta función cambia el brillo dependiendo de la luz del lugar en el que esté el ordenador. Y para entornos oscuros **es horrible**.

Hay una opción para desactivarlo **en los ajustes de energía** pero, cómo no, en mi HP no funciona. Así que, como estaba harto, me puse a buscar cómo desactivarlo y, aunque me costó, lo encontré. Para desactivar el brillo adaptable hay que:

1. Abrir `Regedit`. Para hacerlo, pulsa `Win+R` y escribe `Regedit` en la ventanita que te sale. Y pulsa `Aceptar`.
2. En la ventana de `Regedit`, en la parte de la izquierda busca la siguiente carpeta: `HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\Class\{4d36e968-e325-11ce-bfc1-08002be10318}\0000`. Te saldrá algo como esto:![Si no te sale la imagen, algo se ha escacharrao.](/img/brillo_regedit.jpg "Si no te sale algo como esto, vuelve a empezar.")
3. Haz click derecho en el espacio en blanco, le das a `Nuevo` y a `Valor de DWORD (32 bits)`. De nombre le pones `PP_VariBrightFeatureEnable`.
4. Haz doble click en la línea que acabas de crear y asegúrate de que pone `0` en donde dice `Información del valor`.
5. Despúes pulsa `Aceptar`, cierra el `Regedit` y reinicia el ordenador.
6. Disfruta de tu Windows **con brillo fijo**.


Lugar en el que lo encontré: [http://itmishmash.blogspot.com.es/][Fuente]

**PD**: En la fuente dice que sólo funciona con gráficas AMD, pero mi HP tiene una Nvidia y también funciona. Luego **sirve para gráficas AMD y Nvidia**.

[Fuente]: http://itmishmash.blogspot.com.es/2014/04/how-do-i-disable-auto-brightness-on.html
