---
title: "Guía de Git"
date: 2022-10-08T12:07:56-05:00
draft: false
summary: "Aprende qué es git. El sistema de control de versiones más famoso. Controla tus proyectos y colabora con tus amigos de forma asincrona no lineal! Herramienta vital para el desarrollo de software"
description: Controla tus proyectos con Git.
cover:
    image: 'img/posts/Git/git.png'
    caption: 'Git (sistema de control de versiones)'
    alt: 'logo de git'
categories: ["tech"]
tags: ["Git", "VCS"]
---

# Qué es git 🤔

> Git es un sistema de control de versiones distribuido de código abierto diseñado para manejar de forma eficiente desde pequeños a grandes projectos con velocidad y eficiencia.

## Por qué necesito git

Si alguna vez has:
  1. creado algo
  1. guardado
  1. editado
  1. vuelto a guardar

Entonces muy probablemente te has encontrado con la necesidad de tener varias versiones de un archivo ( o varios archivos), por si algo sale mal, por si todo sale mal o por si quieres hacer cambios experimentales. Necesitas tener la seguridad de que existe una copia "**buena**", la copia "**base**", la copia "**buenaBuena**", la "**Buena30000AhoraSi**", etc.. Y al final terminarás con archivos esparcidos por tus carpetas pero con algunos cambios. No sabrás cuál es el último, ni hablar de el orden de todos ellos.

Aqui es donde entra Git, es un asistente, con una excelente memoria. Git te permite mantener una copia de tus archivos, de hecho de los cambios en tus archivos. Controlas a tus archivos, no ellos a ti 💪🏽.

###  Qué hace git 🌠

Con git puedes:
  + guardar tus proyectos
  + mantener un registro detallado de los cambios en tus archivos
  + colocar mensajes y etiquetas en cada versión
  + crear lineas alternas de trabajo (realizar tus experimentos, sin dañar tus otras versiones)
  + colaborar de forma asincrona en la edición de un archivo
  + viajar en el tiempo (revisa tus versiones previas)
  + identificar las diferencias de una versión a otra
  + detectar herrores en tus proyectos (quién, cómo, cuándo y dónde se generó)

## Cómo trabajar con git (básico)

Inicialmente, tendremos que elegir directorio destinado para nuestro proyecto, donde se alojará nuestro repositorio. Una vez elegido, dentro de la terminal ejecutaremos uno de estos 3 comandos:
```bash
#iniciar un repositorio dentro de la carpeta actual
user@pc$ git init  

#iniciar un repositorio dentro de la carpeta dir_repo
user@pc$ git init dir_repo

#clonar un repositorio dentro
user@pc$ git clone ssh_dir
```

Tendremos que identificarnos, proporcionar información de contacto (correo electrónico y nombre de usuario).

```bash
user@pc$ git config --global user.name "tu_nombre"
user@pc$ git config --global user.email "tu_usuario@tu_dominio.com"
```

Luego podremos ejeccutar el siguiente comando:

```bash
user@pc$ git status
```

Y si el directorio ya tenía archivos o agregamos nuevos (agregaré el archivo hello.rb), arrojará información de nuestro repositorio.

```
user@pc$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	hello.rb

nothing added to commit but untracked files present (use "git add" to track)
```
1. La primera línea nos indica que estamos en la rama **master** (más adelante hablaremos de las ramas). Por el momento piensa en ella como la versión principal de tu proyecto.
2. Observamos la leyenda `No commits yet`. Refiriéndose a que no hemos guardado al menos una versión de nuestro proyecto haciendo un `commit`.
3. `Untracked files` nos indica que no hemos *versionado* este archivo en particular.
4. `nothing added to commit but untracked file present...` nos muestra qué ha sido movido al área de Staging (una área de ayuda para marcar los cambios a guardar)

Para guardar nuestros cambios en el repositorio nos apoyaremos de los siguientes 3 comandos comandos (principalmente).

```bash
user@pc$ git add hello.rb
user@pc$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   hello.rb

user@pc$ git commit -m "agregar hello.rb script de ruby
```

`git add <file>` coloca los cambios en el área de staging. Lo comprobamos con `git status` (que estén en staging no significa que hayan sido guardados). `git commit -m "<messgae>"` no permite guardar el cambio en nuesto archivo de forma permanente, adjuntado un  mensaje concreto de nuesto cambio.

Ahora si queremos consultar el historial de nuesto repositorio (proyecto). Empleamos el comando log:




Para saber qué ha cambiado en nuestro proyecto (directorio). Notaremos

En git, tus archivos pueden encontrarse en 4 estados (principalmente). Siendo `untracked`, `modified`, `staged` y `commited`.
Si tu archivo es nuevo, se encontrará *untracked*. Cuando lo agregamos

En el working directory, Staging, local repository, remote repository.

En un inicio, todos los nuevos archivos se van a encontrar 

### Estados en git

+ Area de trabajo
+ Area de Staging
+ Area de repositorio local


Cómo paso de un estado a otro?

### Comandos básicos

Lista de comandos básicos de git

### Conceptos avanzados

Concepto de Branching

#### Branching

#### Repo remoto





# Documentación

Git tiene una gran página de documentación. Donde explican todo lo relativo a su sistema, sus comandos, las banderas de sus comandos, etc. Consúltala [aquí][git doc].



[git doc]:https://git-scm.com/doc
