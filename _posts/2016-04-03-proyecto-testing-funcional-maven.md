---
layout: post
title: Proyecto para testing funcional, con maven
tags: maven functional example java intellij
eye_catch: ""
---

Escribo este post para tener siempre a mano un proyecto mínimo que sirva para empezar con las pruebas funcionales.

Ya hice un post con un ejemplo básico y sencillo pero con este, la idea es tener un proyecto que además 
esté *mavenizado* y que utilice *testNG*.

El proyecto estará mavenizado porque así tendremos una estructura de directorios organizada y nos va a permitir 
realizar tareas de una forma muy fácil como tener localizadas las dependencias que queramos 
(por ejemplo utilizaremos las de selenium), descargar plugins necesarios, etc

Por otro lado, haremos que descargue y utilice testNG puesto que es un framework que nos va a ayudar a organizar 
y gestionar nuestros tests en este proyecto java (lanzar sólo los tests que consideramos críticos, 
sólo los que tienen que ver con una necesidad, relanzar automáticamente los que han fallado...)

Todos los elementos que voy a utilizar: Java8, IntelliJ, Selenium y TestNG.

¡Empezamos!

Creamos entonces un proyecto java básico y lo hacemos con `maven-quickstart`que es un arquetipo o plantilla 
que sirve como base (generamos así la estructura de directorios del proyecto). Para ello:

* **1.**  Primero, desde la linea de comandos hacemos:

```
$ mvn archetype:generate -DgroupId=com.examples -DartifactId=basic-testing-project -DarchetypeArtifactId=maven-archetype-quickstart
```
Con esto, se nos pregunta en dos ocasiones y debemos pulsar ENTER en ambas (marcadas en amarillo):

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/26139694431/in/dateposted-public/" title="arquetipo"><img src="https://farm2.staticflickr.com/1682/26139694431_bb8a5e2b42_b.jpg" width="1017" height="655" alt="arquetipo"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

Esto nos genera una estructura como la siguiente:

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/26180120586/in/dateposted-public/" title="estructura arquetipo maven"><img src="https://farm2.staticflickr.com/1594/26180120586_38ea896651.jpg" width="474" height="385" alt="estructura arquetipo maven"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

Como se puede ver, ya tenemos creado el _pom.xml_, que es el fichero XML que contiene toda la info necesaria para construir el proyecto.

* **2.** Importamos el proyecto en IntelliJ:

```
File > Open
```
* **3.** Si no tenemos Java8, ya va siendo hora de [descargarlo](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html):

```
File > Project Structure > Project > Project SDK
```

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/26113643532/in/dateposted-public/" title="sdk java8"><img src="https://farm2.staticflickr.com/1617/26113643532_7ff22e6c3b.jpg" width="500" height="182" alt="sdk java8"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

* **4.** Ahora vamos a modificar ese `pom.xml`, añadiendo varias dependencias, las dos de selenium y la de testNG:
      
{% highlight java %}
<dependency>
      <groupId>org.seleniumhq.selenium</groupId>
      <artifactId>selenium-java</artifactId>
      <version>2.52.0</version>
</dependency>
<dependency>
      <groupId>org.seleniumhq.selenium</groupId>
      <artifactId>selenium-server</artifactId>
      <version>2.52.0</version>
</dependency>
{% endhighlight %}

{% highlight java %}
<dependency>
      <groupId>org.testng</groupId>
      <artifactId>testng</artifactId>
      <version>6.8</version>
      <scope>test</scope>
</dependency>
{% endhighlight %}

quedando así:

{% highlight java %}
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.examples</groupId>
  <artifactId>basic-testing-project</artifactId>
  <packaging>jar</packaging>
  <version>1.0-SNAPSHOT</version>
  <name>basic-testing-project</name>
  <url>http://maven.apache.org</url>
  <dependencies>
    <dependency>
      <groupId>org.seleniumhq.selenium</groupId>
      <artifactId>selenium-java</artifactId>
      <version>2.52.0</version>
    </dependency>
    <dependency>
      <groupId>org.seleniumhq.selenium</groupId>
      <artifactId>selenium-server</artifactId>
      <version>2.52.0</version>
    </dependency>
    <dependency>
      <groupId>org.testng</groupId>
      <artifactId>testng</artifactId>
      <version>6.8</version>
      <scope>test</scope>
    </dependency>
  </dependencies>
</project>
{% endhighlight %}

* **5.** Además, descargo [chromedriver](https://sites.google.com/a/chromium.org/chromedriver/downloads) y lo incluyo en la carpeta *src* del proyecto.

* **6.** Y sólo nos queda ajustar la clase principal y la clase de test. Yo voy a implantar el *page-factory* que os comentaba en [este post](http://emerrefe.github.io/qa-blog/pagefactory-pattern)

La estructura final sería:

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/135417629@N05/26206267085/in/dateposted-public/" title="estructura final mvn"><img src="https://farm2.staticflickr.com/1582/26206267085_cbae923931_b.jpg" width="1024" height="559" alt="estructura final mvn"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

Y listo, sobre el test `testMethod` de la clase `TestExample`, click and run!! 
Ya podemos lanzar las pruebas.

## RESUMEN (Para la vagancia)
El [proyecto completo](https://github.com/emerrefe/basic-testing-project/archive/master.zip)
Y las url necesarias para descargar [chromedriver](https://sites.google.com/a/chromium.org/chromedriver/downloads) 
y [SDK Java8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)


**PD.** Podemos ir más allá y tener siempre la última versión de chrome driver descargada utilizando plugins para maven como 
[este](https://github.com/webdriverextensions/webdriverextensions-maven-plugin)

De igual manera, sería modificar el `pom.xml` para que construya el proyecto como nosotros queramos antes de ponernos a lanzar pruebas. Interesante :)

**Nota.** Si podemos ir actualizando el `pom.xml`, mejor. Hay que revisar a menudo si hay versiones nuevas de Selenium y TestNG para ver si, al acogernos a una versión más nueva, todas las pruebas nos siguen funcionando. Además si han introducido mejoras o funcionalidades nuevas, probar a utilizarlas.
