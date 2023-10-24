*ENGLISH*


# :book: Jon Mircha course: responsive design & CSS arquitecture

You can see the video [here](https://www.youtube.com/watch?v=udGrXWeJp1Y&list=PLvq-jIkSeTUZYcX9SYwVe7f66afwd9qk_&index=5)

---

## Tech Stack 🛠️

**HTML5** & **CSS3**


[You can take a look of the proyect here.](https://eugenia1984.github.io/responsive-arquitectura/)

---

# Please: 🎁

- Shared this content with others 📢

- Invite a beer 🍺 or a coffee ☕ to someone from the team

- Thank you very much 🤓.

- Notes: 

I appreciate your interest in this repository ⌨️ with ❤️ by [María Eugenia Cost](https://github.com/eugenia1984) a 😊 and follow me on[LinkedIn - maria-eugenia-costa](https://www.linkedin.com/in/maria-eugenia-costa/)


---
---


*ESPAÑOL*

# :book: Curso de Jon Mircha : diseño responsivo y arquitectura CSS

Podés ver el vidoe de Jon [acá](https://www.youtube.com/watch?v=udGrXWeJp1Y&list=PLvq-jIkSeTUZYcX9SYwVe7f66afwd9qk_&index=5)

---

## Stack teconológico 🛠️

**HTML5** y **CSS3**

[Podés ver el proyecto del curso acá](https://eugenia1984.github.io/responsive-arquitectura/)

---

## Por favor: 🎁

- Compartí este contenido con otros 📢

- Invita una cerveza 🍺 o un café ☕ a alguien del equipo

- Muchas gracias 🤓.

## Notas: 

Aprecio tu interés por este repositorio ⌨️ con ❤️ de [María Eugenia Cost](https://github.com/eugenia1984)  😊 y seguime en [LinkedIn](https://www.linkedin.com/in/mar%C3%ADaeugeniacosta/)

---

# Acá voy a ir dejando notas de la teoría


## :book: REsponsive Design

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

## Breakpoints

Están relacionados con las **media queries**, son los puntos de quiebre para determinar que determinado estilo se va a plicar en determinado tiempo, por ejemplo acorde al ancho de la pantalla, si es mobil lo puedo ver de un modo, si es tablet de otro y si es desktop de ootr, si le puse 2 breakpoints.

En el libro de Ethan Marcot ya nos sugería unas medidas para el responsive design:

- 320px para dispositivos con pantallas pequeñas. como los telefonos en modo vertical

- 480px para los dispositivos con pantallas pequeñas, como los telefonos en modo horizontal; o los mobiles de gama alta en modo vertical.

- 600px para tablas pequeñas. como el kindle

- 768px para tabletas de diez pulgadas como el iPad, en modo vertical

- 1024px para tablets como el iPad en modo horizontal

- 1200px para pantallas panorámicas, como laptops o desktops.

En general por más que tenga una pantalla de 1900px, se suele dejar el contenedor a 1200px, para que no tengamos la mala experiencia en la lectura que tengamos que ir moviendonos de un lado para el otro, si se le podria aplicar el maximo de ancho a la hero-image o a algún mensaje que quiera llamar la atención, se le puede poner una imagen de fondo la 100% y el contenido igual que llegue a los 1200px.

El standard de hoy van de 1200px a 1500px.

Hay sitios que suelen aprovechar el 100% de la pantalla, como las páginas de documentaciones, porque suelen tener en la columna izquierda como un indice, en el medio su contenido y en una columna de la derecha algun resumen o algo que quieran destacar.


Muy importante **conviete tus breakpoints en pxs a ems**, ya que los pixeles son en medidas absolutas y las computadoras que tiene mayor densidad de pixeles y no se visualizan correctamente. Asi es todo relativo la contenedor en el que está.


Objetivo en pixeles / Contexto en pixeles = Resultado en **Ems** : 

```
- 320px / 16px = 20em
- 480px / 16px = 30em
- 600px / 16px = 37.5em
- 768px / 16px = 48em
- 1024px / 16px = 64em
- 1200px / 16px = 75em
```

---

## Viewport

Es una etiqueta que la introdujo Apple, en SAfari para mejorar la presentación de los dispositivos como el iPhone, iPod Touch o iPad.

La etiqueta **viewport** es el área visible de nuestro navegador y permite definir el ancho, alto y escala del area usada por el navegador para mostrrar su contenido.

Tiene 6 atributos importantes:

- **width**: define el ancho visible, suele usarse la constante device-width para que se adapte al ancho del dispositivo.

- **height**: define el alto visible, suele usarse la constante device-height para que se adapte al alto del dispositivo.

- **initial-scale**: define la escala inicial a la que deberá visualizarse el contenido, siendo 1 el 100%.

- **minimus-scale**: define la escala mínima a la que se podrá hacer zoom al contenido, por ejemplo si se configura .5 significa que se podrá hacer un zoom de hasta el 50%. Para controlar hasta donde el usuario hace zoom, para que no se rompa la maquetacion.

- **maximum-scale**: define la escala máxima a la que se podrá hacer zoom al contenido, por ejemplo si se configura 3 significa que se podrá hacer un zoom de hasta el 300%.

- **user-scalable**: define si el usuario puede escalar o no el contenido, sus valores son *yes* por defecto y *no* para bloquear esta propiedad. Es una propiedad booleana. 

Al ponerle no impido que el usuario haga zoom in o zoom out, pero el usuario final está por sobre todos y su interacción es lo más importante, y si le saco el zoom, en un celular no van a poder ampliar la pantalla, lo cual va a ser un inconveniente para alguien con alguna discapacidad visual, lo cual es malo en cuanto a la experiencia de usuario.

Si es por ejemplo un e-comerce, si le sacas el zoom, podes perder al cliente.

El **width** e **initial-scale** son muy importantes para que el contenido se adapte al tamaño del dispositivo.


Separados por **coma** puedo utilizar más de un viewport.

---

## Responsive Grid

Como los Framework de Bootstrap y Foundation tienen las 12 columnas.

El primero de todos fue 960 grid system, centraba el sitio a 960 px y dejaba margen derecho e izquierdo para llegar a los 1024px. En este caso usaban 16 y 12, que eran multiples muy fáciles para dividir en columnas. Y al final se quedaron con las **12 columnas**.


Tamaño (media queries) - Grid artesanal

```
xs - extrasmall -     0     -   479px   - 480res
sm -  small  -   480(30em)  -   767px   - 800res
md -  medium  - 7968px(48em) -   991px  - 800res
lg -  large  -  992px(62rem) -  1199px  - 1280res
xl - extralarge - +1200px(75em)          - 1281res
```

---

## Feature queries

Son reglas *CSS* que le preguntan al navegador si soportan o no, una determinada propiedad o valor. 

Por ejemplo:

```CSS
 @supports (display: grid) {
  /* 
      Código CSS que se aplicará cuando se cumpla la feature queries
  */
}
```

```CSS
@supports (grid-template-columns: subgrid) {
  html {
    background-color: var(--black);
    color: var(--greenyellow);
  }
}
```

Para aplicar estilos cuando NO soporta una determinada característica, se utiliza **not**

```CSS
@supports not (grid-template-columns: subgrid) {
  html {
    background-color: var(--white);
    color: var(--red-dark);
  }
}
```

Como son condiciones lógicas, puedo hacer más de una condición, por ejemplo:

Al utilizar el **AND**, ambas condiciones deben ser verdaderas para aplicar los estilos

```
@suports (display: grid) and (grid-template-columns:subgrid) {...}
```

Al utilizar **OR**, solo debe soportar uuna de las condiciones, por ejemplo:
```
@suports (display:grid) or (grid-template-columns:subgrid) {..}
```

Para ver si las propiedades son soportadas por los navegadores se pueden ver en la web de [Can I Use](https://caniuse.com)

Antes se utilizaba una librería de Js con modernizer, pero gracias a los standares de CSS nuevos, con las features queries ya le damos el soporte.

---

## Containers queries (Consulta de contenedores)

Otra opción para el Responsive Design, porque como las **media queries** permiten hacer cambios dependiendo dle tamaño de la pantalla o de ciertas aracterísticas del dispositivo en que nos enocntramos y las **feature queries** nos permiten aplicar ciertas reglas css dependiendo del soporte de algunos atributos y propiedades, los **containers queries** nos van a permitir redimensionar un contenido en particular.

Con containers queries se piensa un contenido en componente, en vez de que ele elemento de la interfaz dependa del tamaño de la pantalla, dependa más de sus necesidades, como el ejemplo de una  tarjeta que tiene una imagen en vertical hasta que su tamaño es de 300px y luego esa imagen cambia a un formato  en vertical para mostrar su contenido; va a depender de sus propias necesidades.

Es una propiedad bastante nueva (como la de anidación de cósigo css, como se trabaja con los pre procesadores como SASS) y hay varios navegadores que no lo soportan y en otros está en modo experimental.

Para ver más sobre este tema:

[CSS Container Queries MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Container_Queries)

[The new responsive](https://web.dev/new-responsive/) 

[Say Hello To CSS Container Queries](https://ishadeed.com/article/say-hello-to-css-container-queries/) 

### Sintaxis

```CSS
 .card {
    contain: layout inline-size style;
  }

  @container (min-width: 600px) {
    .card-container {
      display: flex;
    }
  }
```

**layout** vas a activar la capacidad de container queries

**inline-size** vas a trabajar con los ejer del contenido

**style** le da la capacidad de poder modificar cualquier propiedad css que este involucrada

En vez de usar @media lo activamos con **@container**. Y si este estilo se lo aplico a un elemento contenedor, entonces los elementos hijos van a heredar el mismo estilo.

--

## SEO : Search Engine Optimization

### Mobilegeddon

Es la actualización al algoritmo de **Google**, que está activo desde el 21 de abril de 2015.

Solo afectan a las busquedas en Google desde el mobil. Siguiendola se sube en el posicionamiento orgánico.

Teniendo en cuenta el auge imparable de los dispositivos móviles y el impacto que éstos están teniendo en las costumbres de uso de la *web*, *Google* hizo un comunicado a través de su [blog oficial](http://googlewebmastercentral.blogspot.com.es/2015/02/finding-more-mobile-friendly-search.html) comentando algunas de las novedades que trae la actualización de su algoritmo.

**Mobilegeddon** pretende actuar sobre todas aquellas webs que no sean amigables con los dispositivos móviles, es decir que no se adapten de forma óptima a dichos dispositivos. 

Dado que las estrategias de *Google* se enfocan cada vez más hacia estos dispositivos, es normal que el buscador quiera asegurarse que las *webs* que indexa cumplen los mínimos de calidad para móviles.

Mobilegeddon, afecta: 
      
- Exclusivamente a las búsquedas realizadas desde dispositivos móviles.
        
- La aplicación del algoritmo será en todos los idiomas y de forma global.

- No se aplicará a sitios webs completos , sólo a las páginas que no cumplan los criterios.

Buenas prácticas de *SEO* y *Responsive*, según *Google* :

[Guía de Google para sitios móviles](https://developers.google.com/webmasters/mobile-sites/?hl=es)

[SEO para mobiles](https://developers.google.com/webmasters/mobile-sites/mobile-seo/?hl=es)

[Mobile Friendly Tes](https://www.google.com/webmasters/tools/mobile-friendly/)

[PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)

---

## Estrategias de Diseño Multidispisitivo

Ethan Marcot:

- Grids Flexibles 

- Imágenes Flexibles

- Media Queries

### Destop First (Graceful Degradation) vs Mobile First (Progressive Enhancement)

**Destop First**: las media queries se deben definir de la mayor a menor. Se utiliza la propiedad **max-wodth** para definir las mediaqueries.

Primero diseñas para Desktop y con las mediaqueries adaptas al celular. Esto se usaba antes poque primero se pensaba para ver en computadora.

Se lo nombro degradación elegante porque al pasar de desktop a mobile en general se le iban quitando cosas o contenido a las interfaces para que se vea mejor en celulares.

**Mobile First**: las media queries se deben definir de la menor a la mayor. Se utiliza la propiedad **min-width** para definir las mediaqueries.

Ahora se suele utilizar esta técnica, porque se ve más todo por el celular.


### Adaptive Design

Trata de crear interfaces que se adapten a las capacidades y características de cada dispositivo ( Hardware y Software).

Utiliza programación JavaScript para los cambios en la interfaz.
 
Además podría tener diferentes fronts dependiendo de los dispositivos que soliciten el recurso, por ejemplo: 

[Facebook Desktop](https://facebook.com/) 

[Facebook Mobile](https://m.facebook.com/) 

[Propuesto en el blog](https://blog.easy-designs.net/archives/on-adaptive-vs-responsive-web-design) de [Aaron Gustafson](https://www.aaron-gustafson.com/)


Conviene en aplicaciones interactivas, como el ejemplo de Facebook. No sería conveneinte aplicarlo si tenes un sitio informativo.


### Responsive Design + Server Side Components  (RESS)

Trata de crear interfaces que se adapten a las capacidades y características de cada dispositivo (Hardware y Software).

Pero a diferencia del *Adaptive Design*i>, la programación que usa esta del lado del servidor. Las interfaces se crean desde el *backend*, lo que permite usar la misma vista (ruta) para todos los dispositivos.

Mandar un front dinamico, sin tener diferentes subdominios.

Fue propuesto por [Luke Wroblewski](https://www.lukew.com/) que escribió un [artículo](https://www.lukew.com/ff/entry.asp?1392). Y tamibén [Getting started with RESS](https://www.creativebloq.com/responsive-web-design/getting-started-ress-5122956).


### Responsible Responsive Design

Mientras que el **Responsive Design** se basa en buenas prácticas de *CSS* para adaptar el contenido del documento *HTML* al tamaño de pantalla del dispositivo que lo visualice, el **Responsible Responsive Design** agrega buenas prácticas de programación *JS* no sólo para adaptar el contenido a la pantalla, sino también para mejorar el rendimiento y la carga de la interfaz en el navegador  *web*.

Fue propuesto por [Scott Jehl](https://scottjehl.com/) que se centro en la mejora de las interfaces a partir de la web performance.


### Fluid Design

Propuesto por [Trys Mudford](https://www.trysmudford.com/), lo publica en 2020.

Es una técnica de *Responsive Design* que trata de escalar y adaptar el contenido al tamaño de la pantalla, sin la necesidad de ocupar  *media queries*.

En lugar de diseñar para un determinado número de *breakpoints*, el *Fluid Design* crea un sistema dentro del cual los elementos escalan de manera proporcional y fluida.


Utiliza características y funciones modernas de *CSS* para hacer fluir las interfaces (sin usar media queries), por ejemplo:
      
- Contenedores fluidos

- Textos fluidos

- [Grids responsivas sin media queries](https://youtu.be/inVlqjPNmD8?list=PLvq-jIkSeTUY628cyd9LVbXSXi2xG9mUl&t=858)   

- Uso de funciones como calc, min, max, clamp

- Uso de unidades relativas como: ems, rems, exs, chs, %, unidades de viewport


Más información:

[Utopia. Fluid Responsive Design](https://utopia.fyi/)

[Utopia Blog](https://utopia.fyi/blog)

[Designing with fluid type scales](https://utopia.fyi/blog/designing-with-fluid-type-scales/)

[CSS-only fluid modular type scales](https://utopia.fyi/blog/css-modular-scales/)

[Fluid type calculator](https://utopia.fyi/type/calculator/)


Ejemplo en codigo para hacer una **grid fluida**

```CSS
.fluid-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}
```

```HTML
<section class="fluid-grid">
  <article class="fluid-item">Elemento 1</article>
  <article class="fluid-item">Elemento 2</article>
  <article class="fluid-item">Elemento 3</article>
  <article class="fluid-item">Elemento 4</article>
  <article class="fluid-item">Elemento 5</article>
  <article class="fluid-item">Elemento 6</article>
  <article class="fluid-item">Elemento 7</article>
  <article class="fluid-item">Elemento 8</article>
  <article class="fluid-item">Elemento 9</article>
  <article class="fluid-item">Elemento 10</article>
  <article class="fluid-item">Elemento 11</article>
</section>
```

Ejemplo en código de **texto fluido**:

```CSS
/* @link https://utopia.fyi/type/calculator?c=320,21,1.2,1140,24,1.25,5,2,&s=0.75|0.5|0.25,1.5|2|3|4|6,s-l */

:root {
  --step--2: clamp(0.91rem, 0.89rem + 0.10vw, 0.96rem);
  --step--1: clamp(1.09rem, 1.05rem + 0.21vw, 1.20rem);
  --step-0: clamp(1.31rem, 1.24rem + 0.37vw, 1.50rem);
  --step-1: clamp(1.58rem, 1.46rem + 0.59vw, 1.88rem);
  --step-2: clamp(1.89rem, 1.71rem + 0.89vw, 2.34rem);
  --step-3: clamp(2.27rem, 2.01rem + 1.29vw, 2.93rem);
  --step-4: clamp(2.72rem, 2.36rem + 1.83vw, 3.66rem);
  --step-5: clamp(3.27rem, 2.75rem + 2.56vw, 4.58rem);
}

.step--2 {font-size: var(--step--2);}
.step--1 {font-size: var(--step--1);}
.step-0 {font-size: var(--step-0);}
.step-1 {font-size: var(--step-1);}
.step-2 {font-size: var(--step-2);}
.step-3 {font-size: var(--step-3);}
.step-4 {font-size: var(--step-4);}
.step-5 {font-size: var(--step-5);}
```

```html
<p class="step--2">Step -2</p>
<p class="step--1">Step -1</p>
<p class="step-0">Step 0</p>
<p class="step-1">Step 1</p>
<p class="step-2">Step 2</p>
<p class="step-3">Step 3</p>
<p class="step-4">Step 4</p>
<p class="step-5">Step 5</p>
```

Un hack para hacer el mismo efecto, pero sin generar tantas clases, que lo usa Ethan Marcott.

```CSS
body {
  /*
    14 = tamaño de letra más pequeño que quieras para tu sitio
    18 = el tamaño de letra más grande que quieras para tu sitio
    1400 = tamaño de viewport más grande
    300 = tamaño de viewport más pequeño, el tamaño de pantalla al que el texto deja de fluir
  */
  font-size: calc(14px + (18-14)*((100vw-300px)/(1400-300)));
}
```


Ejemplo en código de **contenedores fluidos**:

```CSS
.box-fluid {
  width: clamp(400px, 660vw, 600px);
  height: clamp(200px, 30vh, 300px);
}
```

Le agrego un background-color a .blck-flid para poder verlo más estacado en la web

```html
<div class="box-fluid"></div>
```

---

# :book: Arquitectura de CSS

[Slides](https://jonmircha.com/css)

- Escribir CSS es fácil, escalarlo y amntenerlo no tanto.

- Para mantener organizado nuestro código necesitamos un plan -> **Arquitectura css**

### ¿ Qué es la arquitectura ?

Arte y técnica de diseñar, proyectar y contruir edificios y espacios públicos.

-> aplicando el concepto a CSS : *Técnicas que nos ayudan a organizar y mantener nuestro código ordenado, óptimo y escalable*.

Una buena arquitectura de CSS debe saer:


- Predecible: las reglas se van a comportar como esperas que lo hagan, si aplicas una nueva característica, que solo afecte a lo que quieres modificar, que no modifique lo que ya tenías anteriormente. Ejemplos de esto son Bootstrap y Tailwind que son utility first, afectan un solo valor de CSS, o me cambian el tamaño e la fuente, o me cambia el color, me pone el texto en negrita.

- Reutilizable: se puede utilizar en distintas secciones o elementos, de forma rápida y sin afectar a otros elementos. También como le ejemplo de Bootstrap con btn-info que solo me cambia el color.

- Estable: deberíamos de poder actualizar sin poder afectar otras reglas.

- Escalable: que permita crecer y el cósigo sea fácil de mantener.

### Debemos diseñar sistemas, no páginas

base + layout + module + state (hover, focus, diseble) + theme ( light / black)

Diseña de lo general, todos tienen cabecera, menu de navegacion, se adaptan por columnas, vas a ir de lo general y al pasar de un proyecto a otro solo personalizas detalles.

**Componentes** Nicole Sullivan "It's repeating visual pattern, that can be abstracted into an independent snippet of HTML, CSS and possible JS".

Esto ya lo vemos dentro de Bootstrap que ya nos ofrece botones, barras de navegación, por ejemplo.


**Divide y venceras**

**D:R:Y: - Don't repeat yourself**

- cumple una sola función

- es independiente, si lo quito de la interfaz no la afecta y si le voy agregando cosas a la interfaz tampoco se ve afectado.

- es autocontenido, no permiten que elementos externos afecten su estructura interna y sus componentes internos no afectan a componentes externos.

- es reutilizable, puedo usarlo en otro proyecto, customizando los colores de identidad de marca.

Que solo hagan una cosa, y que la hagan muy bien.

Por ejemplo, is eo un header, voy a encontrar: logo, menu block (las tabs), search block (la parte de busqueda) y authblock (la parte de registrarse con usuario, clave y el boton de logueo.).

### Herramientas CSS para crear sistemas

#### 1.Metodologías:

Nos permiten organizar y nombrar el código.
Son las buenas prácticas, la forma de organizar el código, como guardarlos.

[BEM](https://en.bem.info/) Bloque Evento y Modificador.

Bloque = un componente reutilizable en un a página con una funcionalidad independiente. Un ejemplo es ponerle a la clase el nombre de *error* en vez de *red-text*. Tamibén podés utilizar las clases: *header*, *logo*, *search-form*.

Elemento = una pequeña parte de ese bloque principal. Un ejemplo es el logotipo dentro de una cabecera. Ejemplo en la clase sería *search-form__input* con el doble guion bajo indico que viene el elemento. Otro ejemplo es *sarch-form__button*.

Modificador = Ejemplo *search-form__button search-form__button_disabled*, el guión bajo indica el modificador. Otro ejemplo: *search-form__button search-form__button_size_s*

Es la más utilizada, pero queda bastante berboso con la clase larga que queda.

[SMACSS](http://smacss.com/) Scalable and modular architecture for CSS.

En el link vas a poder leer el libro on line.

Va a separar en capas los estilos de CSS, tiene los estilos bases / layout / modulo (componente: header, footer, etc) / state rules (con los estados: hover, habilitado, focus) / theme rules ( modo dark - light) / changing states (cambio, como por ejemplo lo del menu hamburguesa).

Se lo conoce como 7 en 1: base / lauout / modulos /  estados / temas / cambios / estilos particulares del proyecto


[OOCSS](http://oocss.org/) CSS orientado a objetos, se piensa que todo es un objeto, es como el concepto de componente / bloque / modulos. Un ejemplo es cada parte, cada elemento.

[ITCSS](https://itcss.io/) it css (a sane scalable, managed CSS architecture from CSS Wizardry). Es un triangulo a la inversa, parte de lo general e irnos hacia lo especifico. 

generico -> elementos -> objetos -> componentes -> utilidades

[AMCSS](https://amcss.github.io/) Attribute Modules dor CSS, utiliza data attributes de HTML, necesita internamente una librería JS que lo haga funcionar; inclusive a algunos data atrributes les da valor. En definitiva aca le agregamos JS.

[SUITCSS](https://suitcss.github.io/) Style Tools for UI components, es similar a BEM, solo que lo que BEM llama bloque aca se llama componente, y lo que llama modificador aca se llama asi: *in-animating* y *.MyComponent-part*. EL selector se escribie en UpperCamelCase. Integra las clases utilitarias, entonces por ejemplo tiene *u-textTruncate*, *u-sizeFit*, todo lo que comienza con *u-* es una clase utilitaria.

Y si usas un preprocesador

```CSS
/* npm-installed dependency */
@import "suitcss-utils-text";
/* local dependecy */
@import "/Button":

.MyComponent{}
```

[Atomic Design](https://bradfrost.com/blog/post/atomic-web-design/)
Parte de la tabla periodica de los elementos de HTMl que hizo Josh Duck. Y dice que en el diseño atomico hay que pensar en 5 principios:

1- Atomos:  las etiquetas html solas

2- Moleculas: conjunto de átomos, por ejemplo un label, un input text y un boton que nos dan un componente de busqueda en un header, por ejemplo.

3- Organismos: estructuras más complejas, como una cabecera

4- Templates: cuando se diseñan los wire frames, se dibujan las aereas de donde va a ir el contenido, con lapiz y papel o con Figma o alguna otra herramienta.

5- Páginas: reemplazar por el contenido original

[Pattern Lab](https://patternlab.io/) son componentes, un repositorio de Pat Frost.

[Demos](https://demo.patternlab.io/)


#### 2.Frameworks:

Son marcos de trabajo que nos ofrecen componentes y utilidades de UI, que nos permiten no empezar desde cero un proyecto, nos ofrecen su hoja de estilos y el JS, tiene un starter templates.

[960 Grid System](https://960.gs/)  es el padre de todos, empezo por el 2009- 2010, en ese momento no habia responsive design, la resolucion era de 960px y los que sobraban iban hacia los costados. Tenia grid de 12 y de 16 columnas. Estaba basado en floats.

[Skeleton](http://getskeleton.com/) es un boilerplate (un kit de inicio), es más sencillo. También tiene la reticula de 12 columnas, botones, elementos de formulario. Le siguen dando mantenimiento.

[Pure CSS](https://purecss.io/) Esta dividido en: base / grids / formulario / botones / tablas / menues; va separando en capas el código css, puedo usar algunos componentes y los que no uso los saco. Es herramienta minumalista, es más una librería.

[Ink](https://ink.sapo.pt/) no es de los más populares, tien sus propios nombres de clases, se puede descargar el cósigo fuente y modificarlo (por ejemplo le puedo cambiar los breakpoint y las media queries).

[MUI](https://www.muicss.com/) basado en Material Design, si trabajas con Angular, React,  View  o Web Components, lo podes incorporar a tu stack de trabajo. También para email marketing.

[Semantic UI](https://semantic-ui.com/) utiliza las etiquetas semanticas, los elements son los componentes. 

Estos que siguen son los que más se usan:

[Bootstrap](https://getbootstrap.com/) es de los más utilizados, tiene muchos componentes y utilidades que son responsivas. Tiene accesibilidad HTML. En la nueva versión le agregaron hasta iconos, que podes copiar como etiqueta svg, como icono; tienen igonos de interfaz de usuarios y de las redes sociales. La documentación es completa y muy clara. Brinda un starter template. Trae un flujo para instalarlo y configurarlo con Webpack. Su código fuente esta escrito en SASS, lo puedes personalizar, está separado en capas. Utiliza :roots (custom properties, por ejemplo con los colores). La grid de bootstrap funciona con flex box (con las clases row y col, y los breakpoints que tiene). 

Tiene gran cantidad de componentes. Hay una parte específica para los formularios. Y tiene clases auxiliares (**helpers**), por ejemplo con el posicionamiento sticky que además lo puedo personalizar acorde al breakpoint, por ejemplo lo puedo hacer sticky en sm y fixed en md. **FlexBoxx** tiene mapeadas todas sus propiedades, y además están personalizadas acorde al tamaño de la media query. También hay una parte de **padding** y **margin**. También tiene **gap**.

Tiene buenas prácticas e accesibilidad, como rol, area-label. Lo único que tiene como negativo es que utiliza bastantes div, en vez de etiquetas semánticas.

Es un framework utility first.

Lo único que tendría como para mejorar es que las media queries siguen siendo en px, en vez de en ems.

[Tailwind CSS](https://tailwindcss.com/) viene creciendo bastante su uso, tiene pocos años y va ganando popularidad ya que es fácil de implementar en cualquier flujo de trabajo. Es utility first, sus clases aplican a una sola propiedad de CSS (x ej aplica un color de letra, cambia el tamaño de la letra, agrega un padding). Es responsivo. También se puede instalar via npm, tiene hasta su propia lista de comandos; pero también podés incluirlo con CDN. Está muy integrado, con Vue, Gatsby, Nextjs, Laravel, Create Real App, por ejemplo.

[Foundation](https://get.foundation/) Tiene accesibilidad HTML. Tiene bastantes años. Sirve para email marketing y otra versión para sitios. Es semántico, mobile first, configurable. Todas las secciones tienen video tutoriales, además de la documentación y las referencias a SASS (porque podes descargarlo y personalizarlo). Tiene muchos elementos. Está separado en capas: utilidades, colores, selectores, valores, etc. Pero.. Bootstrap le gana en utilidades y componentes.

[Materialize CSS](https://materializecss.com/) implementa el lenguaje visual de Google, solo tiene la version 0 y la 1. Fue el primer framework que dejo de usar jQuery, solo se necesitaba al hoja de CSS y de JS. Se usa mucho para los **componentes de formulario**.

[UI kit](https://getuikit.com/) se utiliza bastante con React. Va ganando adeptos. Es parecido a MUI, es facil de implementarlo a un stack de REact, sus dependencias son el codigo CSS y JS y otro archivo para los iconos. Tiene muchos componentes. En vez de usar nombres genericos sus clases comienzan con *uk-*. Se parece a una interfaz Android. El codigo fuente esta escrito con Less y SASS por si lo queres personalizar. Esta separado en capas.
.
[Bulma](https://bulma.io/) Tiene buenas practicas, no te da componentes a nivel de JS (pero si te deja en vanilla Js la sugerencia por si se lo queres agregar), es puro CSS. Es del grupo del creador de VUE JS. Tiene accesibilidad HTML. Podes acceder al codigo nativo armado en SASS para modificarlo.

#### 3.Procesadores:

Pre procesadores: Son herramientas que toman un lenguaje y lo transforman en CSS. Son meta lenguajes, tiene una sintaxis espefícica que se transpila y se transforma en css, lo que tiene de extra es que agrega funcionalidaddes que css no tiene (como antes que no tenía variables, o determinadas funciones-**mixing**-). 

Permite el **nesting** con el **$**, aunque en CSS todavía esta en parte experimental, ya al menos está en brief a nivel teorico (se trabaja a nivel técinco, en algún momento se irá implementando).

En general los frameworks tienen su código en SASS. 

Permite tener mejor organizado el código css dle proyecto.

Y queda una sola hoja de estilos y minificada.

[Sass](https://sass-lang.com/) es la que más se usa de los tres. Hay archivos que terminan con **scss** que es la sintaxis super css que es similar a css nativo. Es una gema de Ruby y tiene la versión en Node.js. Con **$** se declaran las variables.

Los **partials** son los modulos, pero no importar todo, sino lo que voy a usar.

[Less](https://lesscss.org/), es un paquete de Node de Js, que se debe ejecutar desde una terminal de comandos, hay que instalarlo y una hoja de estilos de less se compila a css. Tiene también el nesting (anidación de CSS).

[Stylus](https://stylus-lang.com/), puede hacer ciclos, crear funciones, hacer calculos aritméticos.

Post procesadores: Son herramientas que procesan el CSS y lo optimizan y automatizan. Por ejemplo que le agregue los prefijos -moz, -o, a todo lo que desde hace un año todavía no es estable; otra cosa que se podría hacer es minificarlo.

Lo puso en el ojo **autoprefixer** que es el pluggin que agregaba los pre fijos para los navegadores que no soportaban determinada propiedad css.

[Post CSS](https://postcss.org/) Es como una guía de estilos, te recomienda que es lo mejor.

[CSS Next](https://cssnext.github.io/), se adelantan a las nuevas características que todavía no están soportadas en CSS de manera nativa. Por ejemplo antes no se le podía aplicar opacidad a un número hexadecimal, pero ahora ya se soporta. Otro ejemplo es lo de los filtros, pero ahora también ya se soporta. Lo que si todavía no se soporta es la anidación.

[CSS in JS](https://cssinjs.org/?v=v10.9.0), con estilos escritos como si fuese un objeto JS, esto se implementa con React y Angular.

**Herramientas de Automatización para utilizar los pre y post procesadores**:

Build Tools: 

[Node.js](https://nodejs.org/en/) permite ejecutar JS, pero del lado del servidor y para la gestión de dependencias en el lado dle Front End (SASS, Less, Stylus).

[Grunt](https://gruntjs.com/) fue uno de los primeros gestores de tareas (task runner), pero otras lo sustituyeron.

[Gulp](https://gulpjs.com/) para generar flujos de trabajos pequeños.

[Webpack](https://webpack.js.org/) es un bundler, es herramienta de React, es el compaquetador y configurador, puedo compilar en un solo archivo js, o varias hojas css las compilo en una sola, también puedo comprimir imagenes

Online Tools: 

[Code Pen](https://codepen.io/) podes generar pequeños proyectos con HTML, CSS y JS. Creas un *pen* (un proyecto) y lo podes compartir, puedo inclusive seleccionar la sintaxis scss. También soporta EMMET.

[JS Bin](https://jsbin.com/?html,output) es como un editor de codigo, y puedo configurar scss. 

[Autoprefixer CSS](https://autoprefixer.github.io/) se copia la hoja de estilos y genera un codigo post procesado con los pre fijos

[CSS Minifier](https://www.minifier.com/) minifica el código css.

---

**Lo importante es saber las bases de HTML y CSS, ya que tanto las librerías, procesadores como frameworks van a ir variando en el timepo**.

---

#### 4.Guías de Estilos

Colección de elemento y reglas pre establecidas que aseguran la consistencia y coherencia de nuestro código.

Se definen los lineamientos de lo que se va a utilizar, cómo se generan las funciones, los selectores en la hoja de estilo, como se da el formato a las imágenes a utilizar; se aplican a todas los lenguajes y tecnologías.

Algunas que se utilizan bastante son:

[Code Guide](https://codeguide.co/) estandares para desarrollar css de manera sostenible, tiene un temario, la sintaxis y el ejemplo.

Dice que el orden correcto de las propiedades de css es:

1-posisionamiento: position / top / rigth / bottom / left / z-index.

2-box model: display / float / width / height .

3-typografía: font / line-height / color / text-align

4- visual: background-color / border / border-radius

5- misc : opacity

Dice que es preferible usar <link> en vez de @import.

Es de Mark Otto (mdo en twitter, creador de bootstrap).

[W3C Design System](https://design-system.w3.org/) es la propuesta de sistema de diseño de la W3C.

[Website Style Guide](http://styleguides.io/) un repositorio con varias guias de estilos de distintos sitios (recopilación de guias de estilos).

[Airbnb CSS / Sass Styleguide](https://github.com/airbnb/css) es la guía de estilos de Airbnb.

[Idiomatic CSS](https://github.com/necolas/idiomatic-css) creada por **necolas** (el que creo Normalize). 

[CSS Guidelines](https://cssguidelin.es/) es fácil de entender, tiene ejemplo de código.

### Arquitectura minimalista

Jon no suele utilizar ni pre ni post procesadores, utiliza css puro.

Usa una sola hoja de estilos y la divide así

```CSS
/* ********** Custom Properties ********** */

/* ********** Reset ********** */

/* ********** Components ********** */

/* ********** Utilities ********** */

/* ********** Site Styles ********** */
```

**Custom Properties** son las variables de CSS que va a utilizar (las que van en **:root**).

**Reset** para tener margin y padding 0, ya que acorde al navegador unos tiene los 8px, y el *box-sizing* con *border-box*.

**Components** como header, nav, una card, un boton.

**Utilities**, una regla que solo modifica un atributo de css.

**Site Styles** los estilos particulares del proyecto, el detalle y personalización de cada uno.

De este modo se diseña pensando en sistemas y no en páginas: base + layout + module + state + theme

Lo único que iría variando de proycto a otro es el *site style* y me armo como mi propia librería, puedo reutilizar código.

Salvo que uno trabaje en un equipo, ahi te vas a tener que amoldar a lo que usa el equipo. Pero, si trabajas de forma freelance o tenes tus proyectos ahi si sería de ayuda utilizar esta arquitectura minimalista.


[Más información en estado de CSS](https://2020.stateofcss.com/es-ES/technologies/)

---
