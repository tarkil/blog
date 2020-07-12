---
layout: post
current: post
cover: https://lh3.googleusercontent.com/pw/ACtC-3ceddWBWKPfgetCFPY7nrtvXTFgLYYPokZ-01KwVIwhE5VYV7ho7pPgU24OUHJ8MktSNstFMF_ZaajrSNTpvk8KrfO9Ije2KcDXtOdACArTG60lGWFG4adEliaj3PKyIRbg7MDPMG_2F6hgcWFOGTwGvQ=w1400-h617-no?authuser=0
navigation: True
title: Configurando la terminal
date: 2020-07-04 00:00:00
tags: utilidades
class: post-template
subclass: 'post tag-utilidades'
author: tarkil
---
Cada persona es un mundo y cada terminal un universo propio.
<!--more-->
Muchos asocian la terminal de comandos con los monitores monocromo de las décadas de los 60 a 80: pantallas negras con letras verdes carentes de sentido para los neófitos en la computación. Aunque la informática ha avanzado mucho desde entonces, us uso sigue siendo imprescindible en ciertas áreas, como la programación y sistemas. Sin embargo, a día de hoy  no tiene porqué ser fea y aburrida si sabes cómo configurarla.

A modo de ejemplo, aquí os dejo como tengo configurada mi terminal. Lo primero de todos es instalarnos [oh my zsh](https://ohmyz.sh/#install).

> note "Requisito"
> Es probable que necesitéis instalar zsh si no lo tenéis instalado ya.

Una vez instalado, podéis quedaros con la configuración por defecto de la terminal o instalar los [plugins](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins) y [temas](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) que más os gusten o necesitéis. Si queréis dejar la terminal como la mía deberías instalar el tema [powerlevel 10k](https://github.com/romkatv/powerlevel10k), dicho tema admite múltiples opciones de estilos y colores que podemos configurar con el comando `p10k configure`.

> warning "Algunas letras se ven raro"
> Si eso te pasa revisa el apartado de fuentes de la guía de instalación.

En cuanto a los plugins que actualmente uso en el ordenador de casa son los siguientes:

* [zsh history substring search](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/history-substring-search) permite navegar entre el historial de comandos que empiezan igual al texto introducido
* [zsh autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/) ofrece una sugerencia de cómo completar el comando
* [zsh interactive cd plugin](https://github.com/ohmyzsh/ohmyzsh/blob/master/plugins/zsh-interactive-cd/) permite seleccionar de manera interactiva el directorio al que queremos ir.
* [safe paste](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/safe-paste) evita que se ejecute el código que hemos pegado de manera automática.


