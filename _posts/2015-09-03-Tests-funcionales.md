---
layout: post
comments: True
title: Tests funcionales
tags: talks
eye_catch: ""
---

Las pruebas o test funcionales son pruebas específicas que nos sirven para validar que el software hace lo que debe hacer y no hace lo que no debe hacer.
Básicamente se utilizan para determinar que el sofware está funcionando como se especificó.

Hace unos meses intenté explicar esto a mis compañeros de equipo puesto que todos vamos a poner nuestro granito de arena en probar las aplicaciones lo más profundamente posible.


<figure class="half">
	<img src="/images/charla1.jpg?raw=true" alt="">
	<img src="/images/charla2.jpg?raw=true" alt="">
</figure>


Los desarrolladores, con nuestra mente de desarrolladores, tendemos a hacer pruebas unitarias, esto es, probar funcionamientos de tipo: Tengo esta entrada --> debo obtener esta salida.
Pero un test funcional requiere algo más, comprobar una característica por completo, un camino funcional.

De ahí que, si estamos acostumbrados a testear de forma unitaria, no lleguemos a ver "más allá de nuestra nariz" e intentemos probar
nuestra aplicación como si sólo conociésemos el código.

Tenemos que ir más allá, meternos en la piel del usuario que utilizará la aplicación y comprobar los caminos que éste llevará a cabo cuando la maneje.

Plantearnos preguntas:

¿Se puede acceder a esta funcionalidad desde otro sitio? como por ejemplo en el caso
de los registros en webs, a veces, si introduces mal las credenciales a la hora de hacer login, se te redirige a una página donde te invita a registrarte (página distinta a la original de registro).

¿Qué sucede si el usuario accede a este lugar sin hacer antes tal otra cosa? como por ejemplo comprar una canción antes de hacer login ¿te redirige a login?

En fin, mil posibilidades.

Y vosotros, al probar funcionalidades ¿qué os soléis preguntar?

¡A las pruebas!
