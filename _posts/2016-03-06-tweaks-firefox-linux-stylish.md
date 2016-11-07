---
title: Tweaks útiles para Firefox en Linux (con Stylish)
tags: [Firefox, Stylish]
categories: [Linux]
published: yes
---
Si usais **Firefox en Linux**, sabréis que la interfaz funciona bajo GTK (no recuerdo si el 2 o el 3). Y sabréis que esta integración tiende a interferir cuando trasteas con temas oscuros, mostrando por ejemplo letras negras bajo fondo negro en el menú desplegable de la barra de direcciones, **lo cual es ilegible**. Esa es la primera cosa que vamos a arreglar. Para ello necesitaremos [Stylish][Stylish], un **add-on para personalizar la interfaz** de firefox y las páginas web que queramos.

Para hacer que firefox muestre correctamente las letras negras con fondo blanco al usar un tema oscuro, debemos **crear un estilo de Stylish** y poner:
{% highlight css %}
@namespace url(http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul);
#urlbar .autocomplete-textbox-container {
    background-color: -moz-Field !important;
    -moz-appearance: none !important;
}
#urlbar > .autocomplete-history-dropmarker {
    -moz-appearance: toolbarbutton-dropdown !important;
    margin: 0px 3px 0px 5px !important;
}
#PopupAutoCompleteRichResult .autocomplete-richlistitem {
    background: -moz-Field !important;
}
#PopupAutoCompleteRichResult .autocomplete-richlistitem[selected="true"] {
    background: Highlight !important;
}
#PopupAutoCompleteRichResult .autocomplete-richlistitem[selected="true"],
#PopupAutoCompleteRichResult .autocomplete-richlistitem[selected="true"] * {
    color: HighlightText !important;
}
.ac-title {
    color: -moz-Fieldtext !important;
}
#PopupAutoComplete .autocomplete-treebody {
    background-color: -moz-Field !important;
    color: -moz-Fieldtext !important;
}
{% endhighlight %}
Con esto firefox mostrará correctamente todos esos campos que antes mostraba mal (como el desplegable de la barra de direcciones, el de la barra de búsqueda o el de autocompletado).

El segundo fix es para la **barra de scroll**. Si os fijáis, en Windows con Firefox maximizado movéis el ratón al lado derecho de la pantalla, hacéis click y hacéis scroll. Pues en Linux no. La razón es que la barra de scroll **tiene un *borde* de un par de píxeles**, por lo que mover el ratón al lado derecho y hacer click no funciona. Tienes que mover con cuidado el ratón para atinarle a la barra. Como dicen en mi pueblo, "toca los huevos a más no poder".

Para arreglarlo, cread un estilo nuevo en Stylish y pegad esto:
{% highlight css %}
@-moz-document url-prefix(http://),url-prefix(https://){
  scrollbar[orient="vertical"]{
    -moz-appearance:none!important;
  }
  scrollbar[orient="vertical"]:hover{
    -moz-appearance:none!important;
  }
}
{% endhighlight %}
Con esto, la barra de scroll aparecerá sin ese molesto borde, pegada al lado derecho de la pantalla.

Sobre las fuentes, el primero no recuerdo de donde lo saqué y el segundo es cosecha propia tras examinar un montón que decían arreglar la barra de scroll pero cambiaban cosas innecesarias.

[Stylish]: https://addons.mozilla.org/es/firefox/addon/stylish/
