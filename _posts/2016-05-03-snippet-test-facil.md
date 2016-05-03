---
layout: post
title: Snippets, menos es más
tags: tips snippet example java intellij
eye_catch: ""
---

¿Conocéis lo fácil que es escribir ciertas sentencias cuando utilizas un IDE? Por ejemplo, al escribir desde IntelliJ 
en java `sout` + ENTER y que automáticamente se escriba un bonito:

```
System.out.println();
```

Seguro que alguna vez os ha pasado que escribimos tantas veces la estructura de algo, que hasta se hace pesado.

A mi me ocurre con la estructura de los nuevos tests funcionales que implemento. Al utilizar otras herramientas como TestNG y
las anotaciones, debo escribir bastante para generar la estructura básica de un nuevo test. Por ello, si me valgo de estos snippets
es mucho más fácil.

Como ejemplo, os cuento dónde encontrarlos en IntelliJ para que podáis generar los que os apetezca y os faciliten un poco la vida.

Si accedemos a:

```
File > Settings > Live Templates
```

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/26191522353/in/dateposted-public/" 
title="snippet menu"><img src="https://farm8.staticflickr.com/7572/26191522353_2324c8fd42_b.jpg" width="1024" 
height="576" alt="snippet menu"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

Podemos generar un nuevo grupo de estructuras como se observa en la imagen anterior y agregar la pertinente.
También se pueden establecer variables dentro de ese código como he hecho con el nombre del método (el nombre del test).

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/26795448795/in/dateposted-public/" 
title="snippet text"><img src="https://farm8.staticflickr.com/7268/26795448795_43deacdc40_b.jpg" 
width="1024" height="576" alt="snippet text"></a><script async 
src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

Además de esto, habrá que ir abajo a *Define* para definir el lenguaje de programación al que queremos que se aplique 
este snippet.

Hecho todo esto y en este caso de ejemplo, al escribir `nt` (que yo identifico con "new test") y pulsar ENTER (ya que así lo he seleccionado en las
opciones de la derecha), acto seguido se escribirá el código escrito en la cajita inferior y dejará el cursor diréctamente sobre el nombre del test.

¡Fácil y sencillo!
Espero que sea útil.
