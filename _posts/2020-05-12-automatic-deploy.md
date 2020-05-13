---
layout: post
current: post
cover: https://lh3.googleusercontent.com/AZufoxZLlc5oAu5XNTKvhdlDkb-EyFvLEri6s-xa0T_BzNPD0ImkjAhx3hWCCmW-x4j-06qtXCYpKPpx51kvJHuKTrQc-d320wfn1lX7XCLUkEmIV0rtQBGPYszYLo2Zre0wdChlTSg=w958-h423-no
navigation: True
title: De cómo despliego el blog
date: 2020-05-12 10:00:00
tags: jekyll
class: post-template
subclass: 'post tag-jekyll'
author: tarkil
---
A pesar de que estoy de confinamiento, he estado bastante ocupado y no he sacado tiempo para publicar nada. Es una lástima porque una de los objetivos del blog es mejorar mi elocución. Hace bastante que no escribo y noto que estoy algo oxidado. Tal vez, haya sido así siempre y es ahora cuando me doy cuenta. Sin más dilaciones, vayamos al tema que nos ocupa.
Para el despliegue y hospedaje del blog hago uso de [Netlify](https://www.netlify.com/). La razón, como comenté [aquí]({% post_url 2020-04-19-fixing-broken-links %}), era que [GitHub](https://www.github.com) no generaba correctamente los sitios que hacen uso de _plugins_ de terceros. Para desplegarlo seguí la [guía](https://www.netlify.com/blog/2015/10/28/a-step-by-step-guide-jekyll-3.0-on-netlify/#step-2-link-to-your-github) de Netlify. La guía está muy bien explicada, así que voy a comentar los pasos de manera rápida:
 * Lo primero es vincular nuestra cuenta de GitHub con Netlify pulsando en _“New site from git”_  desde [https://app.netlify.com/](https://app.netlify.com/). 
 * Seleccionamos y autorizamos  el servicio de git que usamos. En mi caso GitHub.
 * A continuación, elegimos el repositorio que contiene nuestro blog y lo configuramos:
    * _Branch to deploy_: La rama que tiene el contenido a compilar y desplegar. Generalmente el valor será _master_.
    * En _Basic build settings_ especificaremos el comando con el que se debe de generar la página, así como la ruta donde se guarda el resultado de la compilación.
    * _Team up_: No recuerdo qué valores  había. Seguramente no necesites tocarlo si es una página personal. 
* Finalmente, Netlify intentará compilar y desplegar el sitio.

También, es posible hacer uso de un dominio propio. En este [enlace](https://medium.com/@jacobsowles/how-to-deploy-a-google-domains-site-to-netlify-c62793d8c95e) explican cómo hacerlo con [Google Domains](https://domains.google/).

Ya queda menos para dar por finalizada la “_base del blog_”. Las siguientes tareas que tengo pendientes con el blog son:
 * Elegir un logo y borrar los artículos de ejemplo.
 * Arreglar algunos temas de estilo que no me gustan.
 * Valorar la integración de [ _Discuss_](https://disqus.com/) o seguir sin comentarios.
Es bastante trabajo y me da pereza. Tendré que hacer un esfuerzo o no escribiré nunca nada.

