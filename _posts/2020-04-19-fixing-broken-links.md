---
layout: post
current: post
cover: https://lh3.googleusercontent.com/AZufoxZLlc5oAu5XNTKvhdlDkb-EyFvLEri6s-xa0T_BzNPD0ImkjAhx3hWCCmW-x4j-06qtXCYpKPpx51kvJHuKTrQc-d320wfn1lX7XCLUkEmIV0rtQBGPYszYLo2Zre0wdChlTSg=w958-h423-no
navigation: True
title: Arreglando los enlaces rotos
date: 2020-04-20 19:00:00
tags: jekyll
class: post-template
subclass: 'post tag-jekyll'
author: tarkil
---
La semana pasada comentaba que tenía algunos problemas de enlaces rotos cuando construía el sitio mediante la acción de Jekyll de GitHub. La verdad es que no tenía nada claro cuál era la causa del problema, pues en local se veían perfectamente. 
El error consistía en que muchos enlaces les faltaba una “/” en el _”path”_ de la url.  Ejemplo: `https://tarkil.dev/authorstarkil`, en vez de   `https://tarkil.dev/authors/tarkil`. No solo afectaba a las direcciones de los artículos, sino también a la carga de imágenes, javascripts y hojas de estilos.
<!--more-->
Investigando un poco descubrí que el problema estaba relacionado con la variable `site.baseurl` a la hora de concatenar las urls. La solución aunque trivial, era un poco tediosa: reemplazar ciertas ocurrencias de `site.url` con `relative_url`. Un [_commit_](https://github.com/tarkil/blog/commit/38ecd1f86b2d95e978092b0961a69512cb7d61fa) de ejemplo:

```html
   <link rel="stylesheet" type="text/css" href="{{ site.baseurl }}assets/built/screen.css" />
   <link rel="stylesheet" type="text/css" href="{{ site.baseurl }}assets/built/screen.edited.css" />
```
Que habría que reemplazarlo por
```html
   <link rel="stylesheet" type="text/css" href="{{ 'assets/built/screen.css' | relative_url }}" />
   <link rel="stylesheet" type="text/css" href="{{ 'assets/built/screen.edited.css' | relative_url }}" />
```
Desafortunadamente los enlaces a autores y _tags_ seguían rotos. Tocaba investigar, otra vez. Por fortuna, esta vez la razón aparecía en la propia documentación del tema de _Jekyll_, [jasper2](https://github.com/jekyller/jasper2):  GitHub no soporta el uso de _plugins_ de terceros por motivos de seguridad. Como solución se proponen las siguientes:
* Compilarlo en local y subirlo a GitHub. Esta opción no me gustaba, pues mi objetivo era poder olvidarme de tenerlo que compilar cada vez que haga un cambio.
* Hacer uso de [Travis CI](https://travis-ci.org/). Me parecía una buena idea, hasta que leí el tema de tener que versionar el token de git. En principio está cifrado y no debería de tener mayor problema, pero soy muy paranoico y preferí descartarlo. Seguramente acabe cometiendo alguna burrada más grande.
* La última opción que ofrecían era el uso de [Netlify](https://www.netlify.com/). A diferencia de Travis CI, Netlify no necesita “_pushear_” el resultado de la compilación a GitHub, pues lo aloja ella misma.

Tras el cambio a Netlify, creo haber arreglado todos los enlaces, o eso espero.
En el siguiente artículo contaré cómo configuré Netlify con Jekyll y GitHub. Ya adelanto que fue tan fácil como seguir la [guía](https://www.netlify.com/blog/2015/10/28/a-step-by-step-guide-jekyll-3.0-on-netlify/#step-2-link-to-your-github) que ofrecen.

