*ENGLISH*


# :book: Jon Mircha course: responsive design & CSS arquitecture

You can see the video [here](https://www.youtube.com/watch?v=udGrXWeJp1Y&list=PLvq-jIkSeTUZYcX9SYwVe7f66afwd9qk_&index=5)

## Tech Stack 🛠️

**HTML5** & **CSS3**


[You can take a look of the proyect here.](https://eugenia1984.github.io/responsive-arquitectura/)


# Please: 🎁

- Shared this content with others 📢

- Invite a beer 🍺 or a coffee ☕ to someone from the team

- Thank you very much 🤓.

- Notes: 

I appreciate your interest in this repository ⌨️ with ❤️ by [María Eugenia Cost](https://github.com/eugenia1984) a 😊 and follow me on [LinkedIn](https://www.linkedin.com/in/mar%C3%ADaeugeniacosta/)


---


*ESPAÑOL*

# :book: Curso de Jon Mircha : diseño responsivo y arquitectura CSS

Podés ver el vidoe de Jon [acá](https://www.youtube.com/watch?v=udGrXWeJp1Y&list=PLvq-jIkSeTUZYcX9SYwVe7f66afwd9qk_&index=5)

## Stack teconológico 🛠️

**HTML5** y **CSS3**

[Podés ver el proyecto del curso acá](https://eugenia1984.github.io/responsive-arquitectura/)

## Por favor: 🎁

- Compartí este contenido con otros 📢

- Invita una cerveza 🍺 o un café ☕ a alguien del equipo

- Muchas gracias 🤓.

## Notas: 

Aprecio tu interés por este repositorio ⌨️ con ❤️ de [María Eugenia Cost](https://github.com/eugenia1984)  😊 y seguime en [LinkedIn](https://www.linkedin.com/in/mar%C3%ADaeugeniacosta/)

---

# Acá voy a ir dejando notas de la teoría

## Un poco de historia

- En 1998 teníamos a **WML** ( Wireless Markup Languaje ) y a **WPA** ( Wireless Application Protocol) como protocolos que permiten visualizar el contenido, son hermanos de xml y html. Salen los primeros celulares.

- WML se vuelve el standar, pero luego WML y WPa quedan obsoletos porque en el 2007 nace el **iphone** y *Steve Jobs* marca el standard a seguir en disositivos móbiles, tienen Safari integrado y todo un ecosistema (luego por cuestiones economicas sale el app store).

- En 2008 la w3c crea la **mobile web initiative**. En 2008-2009 sale **HTML5**.

- En 2010 *Ethan Marcotte* crea el concepto de **responsive design**, lo publica en un blog y luego lo edita en un libro (2011).


## Responsive design

**Grid Flexibles**: la reticula debe fluir y adaptarse al dispositivo, como por ejemplo el patrón de tener 1 columna para mobil, 2 columnas para tables y 3 comunas para pantalla desktop.

**Imagenes Flexibles**: que fluyan de acuerdo al tamaño del contenedor, aunque físicamente sean más grandes se adaptan. Esto también aplica para: videos, iframes, post, mapas, videos; todos los elementos multimedia.

**Media Queries**: el aliado número uno, con condicionales se van definiendo estilos para deteminadas medidas o formatos.


## No es solo adaptar el contenido de la pantalla, también es considerar...


... **conexión de red**: wi-fi, 2G, 3G, 4G, 5G.

... **hardware** y **software** de los dispositivos: Sistema Operativo, versiones, memoria, procesador, sensores, etc.

... **interacciones**: con el teclado y mouse, táctiles, por voz, etc.

... **accesibilidad web** : soporte a discapacidades.

Y además de los celulares, hoy en día hay: bands, smart watches, sensores para correr, anillos, google glass, etc.


## Estrategias de Diseño Multidispositivos

[Responsive Design](http://alistapart.com/article/responsive-web-design/) con Ethan Marcott en 2010.

[Adaptive Design](https://blog.easy-designs.net/archives/on-adaptive-vs-responsive-web-design/) con Aaron Gustafson en 2011.

[Responsive + Server Side - RESS](https://www.lukew.com/ff/entry.asp?1392) con Luke Wroblewski en 2011. Las interfaces se mandan a llamar desde un Back End.

[Responsible Responsive Design](https://abookapart.com/products/responsible-responsive-design) con Scott Jehl en 2014. Agrega buenas prácticas de JavaScript para mejorar el performance.

[Fluid Design](https://utopia.fyi/) con Trys Mudford en 2020. Diseño más minimalista, los sitios fluidos utilizando poca media querie, haciendo que fluya la tipografía, el tamaño de los contenedores, los grids. Creo **Sergei Cool**, el static template agnóstico (solo HTML 5 y CSS3).

Más información [Diseño Web en la Era Móvil](https://www.iconos.edu.mx/qrtesis/140171MV.html) la tesis de Jon Mircha.

---

## Contenedores Flexibles

antes se trabajaba con medida fijas (px), pero luego al tener más tamaños de pantalla se comenzó a trabajar con medidas responsivas, como **em** o **rem**.

---