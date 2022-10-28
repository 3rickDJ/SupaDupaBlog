---
title: "Guía de MarkDown"
date: 2022-10-02T12:07:56-05:00
draft: false
summary: Descrubre los comandos básicos del lenguaje de marcado MarkDown, simple pero poderoso.
description: Aquí aprenderás los básicos de MarkDown
cover:
    image: 'img/posts/Markdown/logoMarkdown.png'
    alt: ''
    caption: ''
categories: ["tech"]
tags: ["MarkDown", "GoHugo"]

---
# Encabezados

Así como en html tenemos etiquetas para los headers desde `<h1>` --- `<h2>`. En MarkDown utilizamos `# Titulo` para representar un header de nivel `<h1>`. `## Subtitulo <h2>` , `### Subtitulo <h3>`. Así sucesivamente.

```
# Titulo H1
```
# Titulo H1

```
# Titulo H1
```
## Subtitulo H2

```
### Subtitulo H3
```
### Subtitulo H3

```
#### Subtitulo H4
```
#### Subtitulo H4

```
##### Subtitulo H5
```
##### Subtitulo H5

```
###### Subtitulo H6
```
###### Subtitulo H6

## Párrafos

Para escribir un párrafo escribe de forma normal texto. De forma contínua, ya que MarkDown se encargará de formatear tu texto, dando los saltos de línea necesarios. Si quieres escribir en otro párrafo deberás de dejar una línea vacía, entre párrafo y párrafo. Ejemplo:

```md
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Enim neque volutpat ac tincidunt vitae semper quis lectus nulla. Viverra vitae congue eu consequat ac felis donec et odio.

Otro párrafo. Dui id ornare arcu odio ut sem nulla pharetra diam. Augue lacus viverra vitae congue eu consequat ac felis donec. Lorem ipsum dolor sit amet consectetur adipiscing. Dapibus ultrices in iaculis nunc sed augue. Molestie at elementum eu facilisis sed odio morbi.
```

## Formatear texto

### Negritas
Puedes formatear una palabra para que se vea en **negritas** encerrando a la palabra entre dos asteriscos. Ejemplo:

```md
E pour si **move**
```

E pour si **move**

### Itálicas

Similar a las negritas, añade un asterisco antes y después de la *palabra*. Ejemplo:
```md
What does the *fox* say?
```

What does the *fox* say?

### Itálicas Negritas

Si quieres combinarlas, simplemente rodea a la ***palabra*** con 3 asteriscos. Ejemplo:
```md
Aime-moi dans la ***neige***.
```

Aime-moi dans la ***neige***.

## Bloques de Citas

Para crear una cita en bloque, agrega `>` al inicio de un párrafo. Ejemplo:

```md
> We creep up on extinction
```

> We creep up on extinction

### Multiples Párrafos

Agrega un '>' entre cada línea vacía, y a cada párrafo que quieras citar. Ejemplo:
```md
> You put your finest suit on, I paint my fingernails
>
> Oh, we're going out in style. And everything's on sale
```

> You put your finest suit on, I paint my fingernails
>
> Oh, we're going out in style. And everything's on sale

### Combinar Elementos

Combina elementos dentro de una cita. Ejemplo:

```md
> ## Patata
> - Nace
> - *Crece*
> - Se pudre
> - Es venenosa
> - Pierdes
```

> ## Patata
> - Nace
> - *Crece*
> - Se pudre
> - Es venenosa

## Listas

### Listas ordenadas

Agrega un elemento por línea, empezando por el número '1'. Ejemplo:

```md
1. Comida
    1. Burritos
    2. Tacos
2. Agua
3. Aire
```
Equivalente a:
```md
1. comida
    1. Burritos
    1. Tacos
1. agua
1. aire

1. comida
    1. Burritos
    9. Tacos
7. agua
19. aire
```

1. Comida
    1. Burritos
    2. Tacos
2. Agua
3. Aire

### Listas No Ordenadas

Cuando no importa el orden declaramos elementos de nuestra lista con '-', '*' ó '+'. Ejemplo:

```md
- Comida
    - Burritos
    - Tacos
- Agua
- Aire
```
Equivalente a:
```md
* Comida
    * Burritos
    * Tacos
* Agua
* Aire

+ Comida
    + Burritos
    + Tacos
+ Agua
+ Aire
```


- Comida
    - Burritos
    - Tacos
- Agua
- Aire
