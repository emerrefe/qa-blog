---
layout: post
comments: True
title: Testlink, primeros pasos
tags: testlink tips
eye_catch: ""
---

Testlink es una herramienta open-source que nos facilita la gestión de los proyectos de testing que creamos
y además nos ayuda a mantener la calidad de aquello que estamos probando.

Necesitamos un lugar donde escribir todos los tests, todos y cada uno de los pasos a seguir para poder probar 
las funcionalidades y comportamientos de nuestra aplicación (y no podemos pretender tenerlo escrito en un papel). 

Partamos por ejemplo de probar una web donde gestionar usuarios, canciones y listas de reproducción.

He aquí el croquis mental :)

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/24332666856/in/dateposted-public/" 
title="Usuarios"><img src="https://farm2.staticflickr.com/1672/24332666856_2e4b5199ea_h.jpg" width="1600" height="1393" 
alt="Usuarios"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


En testlink nos construiremos nuestra batería de pruebas de esta forma:

**TestSuite:** la colección de tests cases de nuestro proyecto, le pondremos el nombre del mismo.
**TestCases:** cada una de las pruebas software que haremos, con todas las condiciones que deben cumplir
para ver si hacen lo que deben (lo establecido), agrupandolas debidamente.


La idea es tener cada grupo de tests acorde con algún patrón como el Page Object, así para esta web tendríamos tres grandes grupos:

  1.  Gestión de usuarios
  2.  Gestión de canciones
  3.  Gestión de listas de reproducción
(Serán sub-test suites de la test suite principal)

Dentro de estos grupos se tienen distintas "pages" (A, B y C) y distintos test cases como los numerados a continuación.

Centrándonos únicamente en Gestión de usuarios tenemos:

* **(A)** Listado de usuarios
  1.  Buscar usuario por nombre (con resultado exitoso o no)
  2.  Buscar usuario por email (con resultado exitoso o no)
  3.  Buscar usuario por sexo (con resultado exitoso o no)
  4.  Acceder al perfil del usuario

* **(B)** Perfil de usuario
  1.  Editar datos de usuario y guardarlos (con resultado exitoso o no)

* **(C)** Nuevo usuario
  1.  Agregar nuevo usuario (aceptando o cancelando finalmente)
  2.  Agregar nuevo usuario habiendo introducido carácteres no permitidos


A grandes rasgos explico rápido cómo:

- Crear un nuevo proyecto en testlink

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/23742644754/in/dateposted-public/" title="testlink nuevo proyecto 1"><img src="https://farm2.staticflickr.com/1621/23742644754_6de9a64d64_m.jpg" width="1600" alt="testlink nuevo proyecto 1"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/24344620026/in/dateposted-public/" title="testlink nuevo proyecto 2"><img src="https://farm2.staticflickr.com/1549/24344620026_7b974c08d5_m.jpg" width="1600" alt="testlink nuevo proyecto 2"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/23744012553/in/dateposted-public/" title="testlink nuevo proyecto 3"><img src="https://farm2.staticflickr.com/1455/23744012553_0906b6af26_m.jpg" width="1600" alt="testlink nuevo proyecto 3"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

- Añadir test suites (como en el caso de "Mi web", "Listado de usuarios", "Gestión de canciones", "Gestión de listas de reproducción" y las carpetas de "Caminos éxito/fallo" ).

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/24262607252/in/dateposted-public/" title="test suite"><img src="https://farm2.staticflickr.com/1567/24262607252_80d683e7ae_m.jpg" width="1600" alt="test suite"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

- Añadir test cases (caso de todas las pruebas anteriormente numeradas)

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/24344621886/in/dateposted-public/" title="test case"><img src="https://farm2.staticflickr.com/1483/24344621886_62e6ee9cda_m.jpg" width="1600" alt="test case"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

- Añadir pasos a estos test cases (en ellos se pueden incluir notas muy útiles que sirven para determinar cuál es el comportamiento esperado de cada paso)

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/24370831555/in/dateposted-public/" title="pasos y editar tests case"><img src="https://farm2.staticflickr.com/1456/24370831555_479928e8cb_m.jpg" width="1600" alt="pasos y editar tests case"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

Para reforzar aún más la organización de estos test cases, cada test suite puede tener otra división en exitosos o fallidos. En la imagen final se puede observar claramente.

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/24344622906/in/dateposted-public/" title="comportamiento esperado"><img src="https://farm2.staticflickr.com/1587/24344622906_a9ae8cf2ed_m.jpg" width="1600" alt="comportamiento esperado"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

¡Esto es todo por hoy!

Por cierto la imagen del mapa mental del principio no está hecha a mano (aunque lo parezca ^^ )

He utilizado [Balsamiq Mockups](https://balsamiq.com/products/mockups), una interfaz sencilla para plasmar ideas. Me encanta desde que lo descubrí haciendo mi proyecto fin de carrera.

¡A cuidarse!
