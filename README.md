![Banner](imagenes/banner.png)

# M3S3Y4: Fundamentos de HTML y CSS 

> #### **¡Hola, damos inicio al módulo 3!**
> #### Espero te encuentres muy bien y con mucha motivación para continuar el recorrido, supongo que ya tienes instalado todo lo necesario para que tu computadora esté lista para trabajar.
> #### Recuerda que en la U Class pasada debías realizar unas actividades para lograr este objetivo, de lo contrario ingresa nuevamente al contenido, consulta, descarga y realiza las actividades allí señaladas, antes de continuar con este módulo, y una vez tengas tu computadora lista, sigamos adelante.
> #### **Continuemos...**

En esta sesión, iniciamos con los conceptos básicos de HTML y CSS, relativas al desarrollo de interfaces.

# ÍNDICE

- [Fundamentos de HTML](https://github.com/U-Camp/BOOT-M1-SEM1#fundamentos-de-html)
    - [Etiquetas y atributos](https://github.com/U-Camp/BOOT-M1-SEM1#etiquetas-y-atributos)
      - [Formato](https://github.com/U-Camp/BOOT-M1-SEM1#formato)
      - [Enlaces](https://github.com/U-Camp/BOOT-M1-SEM1#enlaces)
      - [Atributos HTML](https://github.com/U-Camp/BOOT-M1-SEM1#atributos-html)      
      - [Imágenes SVG](https://github.com/U-Camp/BOOT-M1-SEM1#im%C3%A1genes-svg)
- [CSS](https://github.com/U-Camp/BOOT-M1-SEM1#css)
    - [Reglas y declaraciones](https://github.com/U-Camp/BOOT-M1-SEM1#reglas-y-declaraciones)
      - [Estructura](https://github.com/U-Camp/BOOT-M1-SEM1#estructura)
      - [Especificidad](https://github.com/U-Camp/BOOT-M1-SEM1#especificidad)
    - [Bordes](https://github.com/U-Camp/BOOT-M1-SEM1#bordes)
    - [Márgenes](https://github.com/U-Camp/BOOT-M1-SEM1#m%C3%A1rgenes)
    - [Padding](https://github.com/U-Camp/BOOT-M1-SEM1#padding)
    - [Fondos](https://github.com/U-Camp/BOOT-M1-SEM1#fondos)
    - [Texto y Fuentes](https://github.com/U-Camp/BOOT-M1-SEM1#texto-y-fuentes)

# Fundamentos de HTML

HTML, es el esquema que define cómo se ordenan los elementos en una página web. No es un lenguaje de diseño de interfaces ni un lenguaje de programación, es un Lenguaje de Marcado de Hipertextos (HyperText Markup Language) que se usa para crear y determinar el contenido de una página web, pero debido a su diseño, no puede definir su funcionalidad, representa visualmente la página web tal cual.

Hipertexto, se refiere a enlaces que conectan una página web con otra, ya sea, dentro del mismo sitio, o entre sitios totalmente ajenos uno de otro.

HTML usa "markup" o marcado para anotar textos, imágenes, y otros contenidos que se muestran en el navegador web. El lenguaje de marcado HTML incluye "elementos" especiales tales como `<head>`, `<title>`, `<body>`, `<header>`, `<article>`, `<section>`, `<p>`, `<div>`, `<span>`, `<img>` y muchos otros más. 

Una estructura básica de un archivo HTML se podría codificar de la siguiente manera:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Título Ejemplo en HEAD</title>
  </head>
  <body>
    <div>Cuerpo en BODY</div>
  </body>
</html>
```

## Etiquetas y atributos

### Formato

Cuando desarrollas HTML, lo primero es entender que existen dos espacios. `head` y `body`.

- `head` es utilizado para establecer todos los metadados de la aplicación.
- `body` se aplica en todas las etiquetas visibles a la interfaz y por ende, al usuario.

Dentro de `body`, las etiquetas estarán compuestas de esta manera:

```html
<body>
  <div id="main">Soy una etiqueta</div>
</body>

```

Se le conoce como **etiqueta** a la apertura y cierre de un espacio. Dentro de la misma, puede establecerse el **contenido** que se visualizará en la intefaz.

Asimismo, existen los atributos que proveen información adicional sobre la etiqueta seleccionada. En este caso `id` es un atributo que contiene el identificador de la etiqueta y su valor sería `main`.


### Enlaces

Los enlaces permiten la navegación por medio de hipervínculos (links) que realizan una conexión y referencian otros archivos o páginas web dentro de la misma aplicación o externa a la misma.

En HTML, los enlaces se marcan con la etiqueta `<a></a>` (de anchor - ancla) y el atributo principal es `*href=""*` donde se escribe la ubicación del archivo de destino que, puede estar en la misma carpeta que el archivo que lo está llamando, en otra carpeta del mismo sitio o, en otro sitio web.

Por defecto, los navegadores web muestran los enlaces subrayados, de color azul si no han sido visitados, de color morado si ya fueron visitados o de color rojo si el enlace se encuentra activo (si está siendo visitado en ese momento).

Entre las etiquetas `*<a href=""></a>*` se puede colocar cualquier elemento HTML que funcionará como botón, generalmente se coloca un texto o una imagen.

Hay distintas rutas de enlace y distintos tipos de enlaces:

  - **Rutas absolutas:** Son aquellas que definen la ubicación completa de un archivo en la web, por ejemplo `http://algo.com/pagina`.
  
  - **Rutas relativas:** Son aquellas que se definen a partir de la posición en la estructura local de la página que lo está refiriendo, es decir, definen la ubicación del archivo de destino con relación a la ubicación del archivo que lo está llamando. 
  
    Ejemplo: si el archivo `index.html` vincula con `ejemplo.html` y están en la misma carpeta, el enlace sería *`<a href="ejemplo.html">Ejemplo</a>`*. 
  
  - **Enlaces externos:** Las rutas enlazadas entre distintos sitios web se les llama enlaces externos ya que hacen referencias a páginas que se encuentran alojadas en alguna otra aplicación web.
  
  - **Enlaces internos:** Son aquellos que pueden ser referenciados relativamente, es decir, dependen de la estructura de carpetas de la aplicación web.
  
  - **Anclas:** Son enlaces hacia un punto determinado dentro de un html. En textos largos, al finalizar muchas veces se coloca un botón para subir. En los sitios de una sola página donde los botones en realidad hacen scroll, esas son anclas. El punto de destino tiene que estar marcado con el atributo id="algo" y en el enlace se coloca un # (numeral) seguido del nombre.  En el ejemplo que se verá a continuación, al dar click en `<a href="#ancla1">Ancla</a>` la página "salta" a este párrafo:  `<p id="ancla1">Esta es un ancla</p>`.
  
  - **Enlaces de correo:** Se puede vincular una dirección de correo para que abra en el programa de correo predeterminado usando la palabra reservada mailto. Ejemplo: `<a href="mailto:info@dominio.com">Contacto</a>`.
  
  - **Enlaces de descarga:** Dentro del atributo href="" se puede colocar la ruta hacia cualquier tipo de archivo. Si el navegador reconoce la extensión, lo abre. Por ejemplo: html, jpg, png, gif, svg, pdf, etc. Pero si no lo reconoce o es un archivo comprimido (.rar, .zip), el navegador le ofrece al usuario descargarlo. Ejemplo: `<a href="archivo.zip">Descarga archivo</a>`.

El atributo target especifica dónde se abrirá el enlace, acepta 4 posibles valores: 

- `_blank` para indicar que se abrirá en una ventana nueva, 
- `_self` para indicar que se abra en la misma página (comportamiento default),
- `_parent` si la página se abrió desde otra página, entonces el enlace se abrirá en la página inicial,
- `_top`, su uso es en iframes e indica que el enlace debe abrirse en la página más elevada del documento principal; los dos últimos son considerados una mala práctica (así como el uso de iframes) y no se recomienda su uso.

>#### ¿Cómo vas?, te recuerdo que puedes volver a leer el contenido cuantas veces lo necesites, es tu primera semana y estás aprendiendo, no te preocupes todo saldrá bien, recuerda lo que te hizo llegar hasta aquí y te queda mucho por aprender. ¡No dudes en preguntar a tus coaches e incluso escribir en teams, es posible que muchos de tus compañeros tengan las mismas dudas que tienes tu. 
>#### ¡Seamos un gran equipo!
>#### :+1:
>#### Continuemos...

# Atributos HTML

La estructura de un documento HTML se basa principalmente en 2 etiquetas principales: 

- `<HEAD />`. Se establecen los metadatos, configuración específica de nuestro proyecto y enlaces internos y externos.
- `<BODY />`. En esta etiqueta, involucraremos todo el contenido del documento. Las etiquetas encontradas dentro de esta, definen el documento visual que el usuario final podrá ver renderizado en su navegador web.

Profundizando dentro de `<BODY />`, vamos a contar con más elementos como `div`, `section`, `article`, entre otras. Estas contarán con atributos globales y contenido (texto plano).

Con respecto a los atributos globales los más importantes son:

**o class:** Una lista separada por espacios de las clases CSS que aplicarán a este elemento.

**o data-*:** Donde el asterisco representa cualquier conjunto de caracteres, su uso es mayormente dado para compartir datos con la interfaz de usuario.

**o hidden:** Indica que ese elemento en particular no se mostrará en la interfaz de usuario.

**o id:** Asigna un identificador global a este elemento en particular, es una referencia al elemento en sí. Debe ser único en todo el documento.

**o style:** Contiene declaraciones de estilo CSS que se aplican específicamente a este elemento.

**o tabindex:** Indica si ese elemento puede tomar el foco y en qué posición (que se pueda seleccionar por medio del teclado o el ratón, los elementos deben llevar una secuencia numérica indicando su nivel de selección), es usado para cuestiones de accesibilidad.

**o aria-*:** Son un conjunto de atributos que se usan para dar accesibilidad a la web a personas con distintos tipos de incapacidades.

**o Event attributes:** Son un conjunto de atributos que pueden usarse para asignar eventos a escuchar dentro de ese elemento, por ejemplo, si el usuario da clic sobre el elemento, se detona un evento el cual puede manejarse por medio del atributo `onclick`.

# Iframes

Los Iframes son una etiqueta especial en HTML `<iframe />` con la que se puede embeber una página dentro de otra página, por lo que permite mostrar una o más páginas dentro de una misma página. Usa los atributos `src` y `title` para definir la URL de la página embebida y un título que se le quiera dar a la misma respectivamente. 

El título no se muestra directamente en la página, si no que este es usado por cuestiones de accesibilidad, para permitir la lectura por screen readers  los cuales leen este atributo para describir lo que se muestra en el iframe. Así mismo, se le puede asignar un tamaño determinado al iframe usando los atributos width y height, los cuales aceptan valores numéricos dados en pixeles especificando las dimensiones del iframe. 

```html
   <iframe
     src="https://wikipedia.com"
     title="Pagina de wikipedia embebida"
     width="400"
     height="200"
   />
```

**Ejemplo de iframe**

Debido a que en la página que usa la etiqueta iframe no se tiene control sobre la página embebida, no es una práctica muy recomendable usar iframes, se debe evitar su uso lo más posible y usarla sólo en casos específicos.


# Imágenes SVG

SVG (Scalable Vector Graphics, Gráficos Vectoriales Escalables) es un lenguaje de marcas basado en XML creado por el W3C y dirigido a la representación de gráficos vectoriales (dibujos y texto).

En un gráfico vectorial, los elementos de la imagen están definidos como formas elementales (líneas, rectángulos, círculos, curvas, polígonos, etc.), definidas mediante etiquetas similares a las del HTML. Por ello SVG no es un formato adecuado para fotografías, pero es idóneo para cualquier tipo de dibujo, técnico o artístico.

Las ventajas de SVG  son muchas:

  - Las imágenes SVG se pueden ampliar a cualquier escala sin perder calidad, ya que están definidas como formas que el navegador dibuja con la precisión necesaria.
  - Las imágenes SVG suelen ocupar poco espacio, ya que están definidas mediante etiquetas. El tamaño en KB de la imagen es además independiente del tamaño con el que se ve en la página web.
  - Las imágenes se pueden reutilizar y combinar fácilmente ya que basta con copiar el código fuente de una imagen a otra.
  - Las imágenes se pueden modificar de forma dinámica mediante hojas de estilo - Javascript porque forman parte de la página web.

Un gráfico SVG puede incluirse en una página web de dos maneras:

  - Objeto Interno: Se puede embeber un SVG directamente en la página, usando la etiqueta `<svg>`, la cual debe contener la definición de los vectores. 

```html
<svg width="100" height="100">
  <circle
    cx="50"
    cy="50"
    r="40"
    stroke="green"
    stroke-width="4"
    fill="yellow"
  />
</svg>
```
_Ejemplo de SVG_

  - **Objeto Externo** Usando la etiqueta `<img>` se puede hacer referencia a un archivo .svg que contenga la definición de una imagen vectorizada. Ejemplo: `<img src="https://s.cdpn.io/3/kiwi.svg" alt="Imagen SVG de un Kiwi">`
  
Desgraciadamente, el uso de SVG se vio frenado porque Internet Explorer no fue capaz de mostrar gráficos SVG hasta Internet Explorer 9 de forma deficiente. 

Actualmente los principales obstáculos del uso generalizado de SVG siguen siendo que las implementaciones en los navegadores todavía son incompletas y los potenciales riesgos de seguridad (debido a que las imágenes SVG pueden contener código Javascript, se recomienda no incorporar imágenes SVG sin haber comprobado antes su contenido).

De cualquier manera, SVG se ha ido imponiendo poco a poco como formato estándar de gráficos vectoriales frente a otros formatos propietarios y numerosos programas de edición de gráficos son capaces de importar y exportar en formato SVG.

```HTML
<!DOCTYPE html>
<html lang="en">
 <head>
   <meta charset="UTF-8">
   <title>Ejemplo HTML</title>
 </head>
 <body>
   <h1>
     Encabezado 1.
   </h1>
   <pre id="ancla">
     Párrafo de texto preformateado que respeta los
     saltos de línea así como los espacios.
   </pre>
   <hr />
   <p>
     Enlace externo con ruta absoluta
     <!-- Enlace externo con ruta absoluta -->
     <a href="https://facebook.com">Facebook</a>
   </p>
   <p>
     Enlace interno con ruta relativa
     <!-- Enlace interno con ruta relativa -->
     <a href="estilos.css">Enlace relativo</a>
   </p>
   <p>
     Enlace ancla
     <!-- Enlace ancla -->
     <a href="#ancla">Ancla hacia el texto preformateado</a>
   </p>
   <p>
     Enlace de correo
     <!-- Enlace de correo -->
     <a href="mailto:algo@dominio.com">Enlace de correo</a>
   </p>
   <p>
     Enlace de descarga
     <!-- Enlace de descarga -->
     <a href="descarga.zip">Enlace de descarga</a>
   </p>
   <hr />
   <h2>
     SVG Embebido
   </h2>
   <p>
     <!-- SVG embebido -->
     <svg width="100" height="100">
       <circle
         cx="50"
         cy="50"
         r="40"
         stroke="green"
         stroke-width="4"
         fill="yellow"
       />
     </svg>
   </p>
   <h2>
     Imagen SVG referenciada
   </h2>
   <p>
     <!-- Imagen SVG referenciada -->
     <img src="https://s.cdpn.io/3/kiwi.svg" alt="Imagen SVG de un Kiwi" />
   </p>
 </body>
</html>
```
_Ejemplo de HTML con SVG_

> #### ¿Qué te pareció el contenido de HTML?. Si quieres te dejo una infografía que resume un poco el tema tratado con HTML la cual podrás consultar y descargar [presiona aquí](https://github.com/U-Camp/BOOT-M1-SEM1/blob/main/infografias/M1_S1_Infografia%2001.pdf) 

> #### Ahora bien, hasta ahora has notado que únicamente hemos hablado y visto la estructura de un documento HTML.
> #### Pero quizás te preguntarás, ¿Cómo se desarrolla el diseño visual de este documento?, para ello iniciamos con el contenido de CSS que sigue a continuación. 

# CSS

**HTML** permite definir la forma en la que se presentarán los elementos dentro de un navegador web, pero no define los colores que se usarán, ni los tamaños o formato de los textos, este estilizado de la página se define con **CSS** .

Las Hojas de Estilo en Cascada (Cascading Style Sheets) son un esquema utilizado para describir la presentación de los elementos HTML presentes en una aplicación web, por lo que CSS describe como debe ser renderizado el elemento en pantalla.

Éstas dos tecnologías forman parte del rendering engine que todos los navegadores web integran para poder interpretar y cargar correctamente una página web, así mismo sus reglas, sintaxis y estándares las define el mismo consorcio W3C, por lo que el estándar debe ser respetado por las compañías que desarrollan cada navegador, se puede decir que el futuro de las dos tecnologías (HTML y CSS) está ligado y tienen el mismo objetivo.

Un ejemplo de un documento HTML que hace uso de CSS para estilizar los elementos se muestra a continuación:

```css
/* Archivo Estilos.css */

/* Se aplica directamente al elemento <body> */
body {
 color: blue;
}
/* Se aplica directamente a todos los elementos de tipo <p> */
p {
 color: red;
}

/* Se aplica en el(los) elemento(s) donde se use */
.clase-css {
 color: black;
}
``` 
_Ejemplo de código CSS_

```html
<!DOCTYPE html>
<html lang="en">
 <head>
   <meta charset="UTF-8">
   <link rel="stylesheet" href="estilos.css">
   <title>Ejemplo HTML y CSS</title>
   <style>
     body { /* Se aplica directamente al elemento <body> */
       color: gray;
     }
     h2 { /* Se aplica directamente a todos los elementos de tipo <h2> */
       color: navy;
     }
     /* Se aplica sólo en el elemento donde se use con el atributo `class` */
     .clase-css-tag {
       color: green;
     }
   </style>
 </head>
 <body>
   <h1>
     Encabezado 1 de color gris.
   </h1>
   <h2>
     Encabezado 2 de color azul marino.
   </h2>
   <p>
     Párrafo para encabezado 2 de color rojo.
   </p>
   <h5 class="clase-css">
     Encabezado 5 de color negro.
   </h5>
   <p class="clase-css-tag">
     Párrafo para encabezado 5 de color verde.
   </p>
   Texto de color gris dentro de body
   <p>Párrafo de color rojo</p>
   <div class="clase-css">
     Texto de color negro.
   </div>
   <p class="clase-css-tag" style="color: orange;">Texto de color naranja.</p>
   <img
    src="https://www.utel.edu.mx/sites/default/files/ingenieria-en-computacion.jpg"
    alt="Texto alternativo para la imagen"
    width="400"
    height="200"
   />
 </body>
</html>
``` 
_Ejemplo de código HTML con código CSS integrado_


> #### Hola, ¿cómo te sientes hasta ahora?, ¿quisierás practicar lo aprendido o ver como se ve en línea?, si tu respuesta es afirmativa, copia y pega el código anterior en Visual Studio Code o ingresando al siguiente link, https://codepen.io/pen/  así podrás validar cómo funciona y allí puedes agregar o eliminar líneas para que vayas practicando lo aprendido. 
> #### Seguimos...


Así como HTML, CSS tampoco es un lenguaje de programación, es un esquema de diseño que permite aplicar estilos de manera selectiva a elementos que se encuentran en documentos HTML. En el ejemplo anterior, la regla p en el archivo estilos.css [para ver el ejemplo estilos.css presiona aquí](https://github.com/U-Camp/BOOT-M1-SEM1/blob/main/ejemplos/index.css) aplica de manera selectiva en todos los elementos párrafo dentro del archivo HTML, lo que convierte el texto dentro de esos elementos en color rojo.

Con esto claro y en vista de cómo se integran, vamos a conocer las características de CSS.

## Reglas y declaraciones

### Estructura

La estructura general del esquema es llamada regla, la cual se compone de los siguientes elementos:

**o Selector:** Comienza la regla, selecciona el(los) elemento(s) a los cuales aplicar el estilo (body, p o .clase-css en el ejemplo).

**o Declaración:** Es una directiva que define las propiedades a cambiar dentro del elemento a estilar. Esta declaración se compone de propiedades, que son los atributos del elemento que se pueden estilar, así como de los valores de esas propiedades, que son las que se asignan después de los dos puntos y especifican la apariencia. (color: blue; color: red; o color: white; en el ejemplo).


### Especificidad


Para hablar de especificidad, primero debemos determinar cómo están enlazados los archivos.

Accede a la carpeta `ejemplos` dentro de este repositorio y verás dos archivos:

- `index.html`. Contiene nuestra estructura base, incluyendo las etiquetas y enlaces externos, es decir a un archivo `index.css` donde contendremos nuestros estilos..
- `index.css`. Contiene nuestra hoja de estilos con selectores y propiedades.

Claro esto, hablemos dentro sobre especificidad.

¿Cómo funciona?

Los selectores son aplicados bajo un esquema de prioridad, es decir, el navegador web ya tiene asociado esas prioridades dentro del motor de renderizado y aplica las reglas dependiendo del lugar en el que se encuentren definidas (especificidad):

  1. Primero, se aplican las reglas definidas en archivos externos (estilos.css en el ejemplo).
  
  2. Segundo, se aplican las reglas definidas dentro de la etiqueta `<style />`, las reglas aquí definidas pueden sobrescribir cualquier regla ya definida en archivos externos (en el ejemplo, dentro del archivo `estilos.css` se define la regla para el body con el color azul, pero dentro de la etiqueta `style` éste se sobrescribe definiéndose como color gris, por lo que, al tener mayor prioridad, prevalece el gris).
  
  3. En tercer lugar, se aplican las declaraciones definidas de manera `inline`, esto quiere decir, aquellas que se escriban directamente dentro del atributo `style` en cada elemento, éstas son individuales y aplican solamente para ese elemento en particular (en el ejemplo, último párrafo con texto de color naranja, éste puede aplicar el estilo para los párrafos p que se define dentro de estilos.css, pero como tiene asignada una clase "clase-css-tag", éste tiene mayor prioridad, sin embargo también tiene asignado el estilo inline con el atributo style, por lo que éste le gana a las anteriores y prevalece el color naranja).
  
  4. Existe la palabra reservada !important, la cual si se aplica a cualquier declaración ésta sube en precedencia y tiene prioridad sobre el resto de las reglas, pero es considerada una mala práctica por que provoca que se rompa el esquema de prioridad de cascada, por lo que no se recomienda su uso.

Como pudiste ver, a partir de esta especificidad y prioridad en la aplicación de estilos es de donde viene el nombre CSS, ya que depende de esa prioridad para aplicar los estilos de manera figurativa a una cascada. 

Como parte de las reglas existen los selectores de clase, este tipo de selectores sólo aplican el estilo en aquellos elementos que se definen dentro del HTML con la palabra `class`, el cual es un atributo de HTML y no debe confundirse con la clase que define a un objeto, ya que son dos cosas diferentes.


## Bordes

La directiva border permite especificar el estilo, tamaño y color del borde de un elemento en particular, se define por las siguientes sub-directivas:

- **border-style:** Especifica el tipo de borde a mostrar, soporta varios valores para distintos tipos de línea de borde: dotted, dashed, solid, double, groove, ridge, inset, outset, none y hidden. Así mismo acepta 1, 2 y 4 valores distintos, dependiendo del lado del borde que se quiere especificar: top right bottom y left. Ejemplo `border-style: dotted;` aplica en los 4 bordes, `border-style: dotted dashed;` aplica dotted para el top y el bottom y dashed para los lados laterales (left y right) `border-style: dotted dashed solid double;` aplica para cada lado (top right bottom left).
  
- **border-width:** Especifica el ancho de cada uno de los 4 bordes de cada elemento, puede estar dado en un tamaño específico (px, pt, cm, em) o usando uno de los tres valores pre-definidos (thin, medium, thick). Así mismo también acepta desde 1, 2 y 4 valores. Ejemplo `border-width: 1px;` aplica en los 4 bordes, `border-width: 1px thin;` aplica 1px para el top y el bottom y thin para los lados laterales (left y right) `border-width: 1px 2px 3px medium;` aplica para cada lado (top right bottom left).
  
- **border-color:** Especifica el color con el que se mostrará el borde. Acepta los mismos valores que la directiva `color`, aceptando además un valor adicional transparent, el cual se aplica para transparencias y opacidades, las cuales se verán más adelante. Ejemplo `border-color: #ff0000;`

Para minimizar el código se pueden especificar todos los valores del borde en una misma propiedad, en lugar de escribir cada una de las directivas, se declara una sola propiedad con todos los valores para cada una de las directivas `border: 5px solid red;`. El orden es `border: width style color` y debe ser respetado.

```CSS
.borde-completo {
 border: 5px solid red;
}

.bordes-laterales {
 /* El orden es top right bottom left */
 border-style: none dotted none dotted;
 border-width: 2px;
 border-color: #00AA00;
}
```
_Ejemplo de Bordes en CSS_


## Márgenes

Los márgenes (margin) representan espacios alrededor de los elementos, es decir, define el tamaño del espacio entre un elemento y otro, el espacio entre sus bordes correspondientes. Esta directiva acepta 4 posibles valores: **auto** con el que el navegador calcula automáticamente el margen de cada elemento (comportamiento default), **una longitud específica** (px, pt, cm, em), un **valor en porcentaje** (%) que es la proporción con relación al elemento superior que lo contiene y finalmente **inherit**, lo cual indica que el elemento hereda el margen definido en el elemento superior que lo contiene.

Se pueden usar las directivas específicas para un margen de cada lado, de la siguiente manera:

  - **margin-top:** Especifica el espacio de margen superior. Ejemplo `margin-top: 2px;`.
  - **margin-right:** Especifica el espacio de margen a la derecha del elemento. Ejemplo `margin-rigth: 1.2em;`.
  - **margin-bottom:** Especifica el espacio de margen inferior. Ejemplo `margin-bottom: 10%;`.
  - **margin-left:** Especifica el espacio de margen a la izquierda del elemento. Ejemplo `margin-left: inherit;`

Igual que con los bordes, se puede minimizar código especificando la directiva `margin` y asignando los valores de la propiedad en el orden en el que se especifican, es decir `margin: 2px 1.2em 10% inherit;`, respetando el orden top right bottom left.

```CSS
.margen-completo {
 /* El orden es top right bottom left */
 margin: 2px 2.2em 2% inherit;
}

.margen-superior-inferior {
 margin-top: 2px;
 margin-bottom: 2.2em;
}
```
_Ejemplo de Márgenes en CSS_

## Padding

La directiva padding se usa para definir el tamaño del espacio alrededor del contenido del elemento, es decir, dentro de los límites de los bordes, desde el borde hasta el contenido en sí del elemento. De igual manera, acepta los mismos valores que la directiva `margin` exceptuando el valor auto, el cual no está soportado, pero sí acepta longitudes específicas (px, pt, cm, em), un valor en porcentaje (%) que es la proporción en relación con el elemento superior que lo contiene y finalmente inherit, lo cual indica que el elemento hereda el padding definido en el elemento superior que lo contiene.

Igualmente, soporta directivas para especificar cada lado padding-top, padding-right, padding-bottom y padding-left, los cuales se usan de la misma manera que los márgenes, así mismo, también soporta el minimizado de código con la directiva `padding: top right bottom left`.

```
.padding-completo {
 /* El orden es top right bottom left */
 padding: 2px 2pt 1% inherit;
}

.padding-por-lado {
 padding-top: 2px;
 padding-right: 10px;
 padding-bottom: 5px;
 padding-left: 1px;
}
```
_Ejemplo de Padding en CSS_


# Colores

Para especificar colores de texto en un elemento HTML usando CSS, se usa la declaración `color`, la cual acepta cualquiera de los 140 nombres de colores predefinidos que los navegadores web tienen integrados  (ejemplo `color: red;`)

Asimismo, puede aceptar valores en RGB:

- RGB: `color: rgb(255,0,0);`
- Hexadecimal: `color: #FF0000;`
- HSL: `color: hsl(0, 100%, 50%);`
- HWB: `color: hwb(0, 0%, 0%);`

# Fondos

Para especificar fondos se usa la declaración `background `, la cual se divide en cuatro directivas:

  **1. background-color:** Para asignar el color de fondo de un elemento, acepta los mismos valores que acepta la directiva `color`. Ejemplo `background-color: #FF0000;.  
  
  **2. background-image:** Especifica una imagen para ser usada como fondo de un elemento en particular. Por default, si la imagen es más chica que el elemento que la contiene, ésta se repite de tal manera que cubra completamente el elemento. Acepta sólo texto con valores de tipo URL. Ejemplo `background-image: url("path/hacia/una/imagen.jpg”)`;
  
  **3. background-repeat:** Como te comenté, el comportamiento que el navegador tiene es repetir la imagen por default hasta llenar el elemento que la contiene, sin embargo, con esta directiva se puede cambiar ese comportamiento, de tal manera que se pueda repetir sólo horizontalmente (ejemplo `background-repeat: repeat-x;`), verticalmente (ejemplo `background-repeat: repeat-y;`) o mostrar la imágen sólo una vez (ejemplo `background-repeat: no-repeat;`).
  
  **4. background-position:** Esta directiva permite establecer la posición de inicio de las imágenes en relación al elemento que las contiene, por default el explorador las ubica en la parte superior izquierda del elemento y a partir de ahí empieza a dibujar la imagen, pero se puede cambiar el comportamiento para que la imagen se ubique en la parte superior derecha (ejemplo `background-position: right top;`), esta directiva acepta 4 posibles valores indicando la posición relativa: left, top, right, bottom.

Para minimizar el código se pueden especificar todos los valores del fondo en una misma propiedad, en lugar de escribir cada una de las directivas, se declara una sola propiedad con todos los valores para cada una de las directivas:

```css
background: #FF0000 url("path/hacia/una/imagen.jpg") no-repeat right top;. 
```

Para que sea correctamente interpretado se tiene que respetar el orden en el que fueron explicadas (`background: color image repeat position`).

# Texto y Fuentes

La mayoría de las páginas y aplicaciones web, usan fuentes de texto específicas que van con una imagen de la marca o de la empresa para la que se está desarrollando la aplicación.

Para poder configurar el texto y que el explorador cargue las fuentes específicas para esta página y las aplique, se usan varias directivas que permiten especificar la familia de la fuente, su tipo, su formato, tamaño y estilo de un texto en específico, las cuales son las siguientes:

  **o font-family:** Establece la familia de la fuente a usar para el texto, puede contener varias fuentes en orden de prioridad por si el navegador no puede cargar alguna o no la soporta intentar la siguiente. Ejemplo `font-family: Arial, Helvetica, sans-serif;`.
  
  **o font-style:** Especifica si se aplica un estilo itálico al texto. Tiene 3 posibles valores: normal, italic y oblique, aunque este último es menos soportado en los navegadores. Ejemplo `font-style: italic;`.
  
  **o font-weight:** Especifica si se aplica un estilo “negrita” al texto. Tiene 2 posibles valores: normal y bold. Ejemplo `font-weight: bold;`.
  
  **o font-size:** Especifica el tamaño del texto. Acepta valores absolutos (como son tamaños estáticos dados en pixeles) o valores relativos (que son dados en proporción al elemento que los contiene). Ejemplo `font-size: 16px;` o `font-size: 2.5em;`.

Para acortar código, es posible usar la directiva `font` directamente y asignar esos valores, no requiriendo estar en algún orden en específico, pero sí, al menos que se defina el tamaño y la familia (ejemplo `font: 12px Arial, sans-serif;`).

> #### ¿Qué te pareción el contenido de CSS?, si deseas puedes consultar y descargar una infografía sobre este contenido, [Presiona aquí](https://github.com/U-Camp/BOOT-M1-SEM1/blob/main/infografias/M1_S1_Infografia%2002%20(1).pdf)

> #### Muy bien, llegamos hasta aquí por ahora, recuerda que puedes hacerle preguntas a tus coaches en caso de ser necesario, leer el contenido nuevamente si así lo deseas y puedes practicar lo aprendido ingresando a este link https://codepen.io/pen/  
> #### Nos vemos en la siguiente semana. :smiley:

