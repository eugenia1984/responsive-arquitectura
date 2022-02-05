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

## Multimedia flexible

img, audio, video, iframe, canvas, svg, picture, object, embed, map, area.

En el Responsive Design la multimedia debe ser flexible y adaptarse al tamaño de su contenedor, lo podemos lograr con las siguiente regla CSS:

```CSS
img, audio, video, iframe, canvas, svg, picture {
          max-width:100%;
          height: auto;
        }
```

### Imagenes

**Atributo srcset y sizes**: para mejorar el rendimiento de carga, al colocar la misma imagen pero en diferentes tamaños y pesos, dependiendo del tamaño o la resolución de la pantalla.

Ejemplo en código:

```html
<img src="img/html5-3d-600.png" srcset="img/html5-3d-600.png 1x, img/html5-3d-900.png 1.5x img/html5-3d-1200.png 2x" alt="icono de HTML5">
```

Para este segundo caso, si se carga la imagen del tamaño más grande no se va a ver la responsividad, pero si se carga del tamaño más pequeño si se nota.

Utilizando el atributo **srcset**. Ejemplo en código:

```html
 <img src="img/html5-3d-600.png" srcset="img/html5-3d-600.png 600w, img/html5-3d-900.png 900w img/html5-3d-1200.png 1200w" alt="icono de HTML5">
```

Utilizando el atributo **srcset** y **sizes**. Ejemplo en código:

```html
  <img src="img/html5-3d-600.png" srcset="img/html5-3d-600.png 1x, img/html5-3d-900.png 1.5x img/html5-3d-1200.png 2x" sizes="(max-width:480px) 300px, (max-width:600px) 480px, (max-width:768px) 600px, (max-width: 1024px) 900px, (min-width: 1200px) 1200px"  alt="icono de HTML5">
```

Muchas plantillas de WordPress lo utilizan, internamente genera varios tamaños de la imagen que subo, genera entre 3 a 5 tamaños, para dependiendo de la resolucion del Theme se utilizan los atributos srcset y sizes.


**Etiqueta picture**: para mostrar diferentes tamaños de la misma imagen, y también mostrar imágenes diferentes. Por ejemplo, recortar una Imagen de forma diferente según el tamaño de la pantalla y las diferencias en el diseño. Esto se conoce como "dirección de arte".

Esto se ve en los sitios que tiene una version minificada de su logo, entoences acorde al tamaño se ve un logo u otro.

Para los navegadores que no soportan la etiqueta **picture** utilizamos al etiqueta **img** con la imagen más pequeña.

Ejemplo en código:

```html
<picture>
  <source srcset="img/kitten-large.png" media="(min-width: 1024px)">
  <source srcset="img/kitten-medium.png" media="(min-width: 600px)">
  <img src="img/kitten-small.png" alt="kitten">
</picture>
```

Pero también tenemos un nuevo tipo de formato **webp**, propuesto por Google, es una mejor solución de imagen para los jpg y gif animados.

```htlm
<picture>
  <source srcset="img/butterfly.webp" type="image/webp"> 
  <img src="img/butterfly.jpg" alt="butterfly">
</picture>
```

### Videos

La forma más clásica de hacerlo responsivo, es con las propiedades:

```CSS
max-width: 100%;
height: auto;
````

Otro modo es utilizando la propiedad **aspect-ratio**.

## Media Queries

Se definen con el formato de la versión 2 con la etiqueta **link**. Por ejemplo, en el **header**:

```html
 <link rel="stylesheet" media="print" href="css/print.css">
```

Y en el css:

```css
@page {
  size: A4;
}

body {
  font-size: 12pt; 
  font-family: serif;
  background-color: #000;
  color: #fff;
}
```

Se usa puntos -pt- porque se imprime con el software de Microsoft Word que trabaja con pt como medida

- Otro modo es con el **css** con las **@media**

Ademá de las clásicas media queries acorde a la medida de las pantallas, como los de las librerias o frameworks,  como las de Bootstrap que tienen por ejemplo: 

Para los diseños MOBILE FIRST
```
@media screen and (min-width: 480px) {...}
```

Para los diseños DESKTOP FIRST
```
@media screen and (max-width: 1024px) {...}
```

Si se empezo un diseño Mobile First no combinar con el diseño Desktop First sino puede haber inconveniente con los estilos, si se usa min-width al principio usar ese y no el max-width.

Y hay otras menos conocidas, como por ejemplo:

- @media print , para impresion

- @media screen and (prefers-reduced-motion: reduce) { } , para inhabilitar el scroll-behavior: smooth;

- @media screen and (prefers-color-scheme: dark) { }, para hacer el efecto dark

- @media screen and (prefers-color-scheme: light) { }, para hacer el efecto light

---

## Braekpoints