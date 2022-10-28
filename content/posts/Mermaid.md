---
title: "Mermaid in Hugo"
draft: true
description: Agrega Mermaid
summary: Una guia de como usar mermaid con goHugo
categories: ["tech"]
tags: [ "diagrams"]
date: 2
cover:
    image: 'img/posts/Mermaid/uses.png'
    alt: ''
    caption: 'close caption?'
---

checar el log de los commits
Lo que recuerdo era agreagar el render-codeblock-de mermaid para setear una variable en la que indicquemos que estamos utilizando mermaid y queremos que sea renderizado de una forma especial
Creamos un partial para agregar nuestro js e injectar todo el texto (contenido dentro del codeblock), con un iff hasmermaid, para solo agregar mermaid cuando sea requerido
Agregar el partial al final de nuestro base.html, porque necesita ser renderizado after hugo scanned


```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
<!-- ```goat -->
<!--       .               .                .               .--- 1          .-- 1     / 1 -->
<!--      / \              |                |           .---+            .-+         + -->
<!--     /   \         .---+---.         .--+--.        |   '--- 2      |   '-- 2   / \ 2 -->
<!--    +     +        |       |        |       |    ---+            ---+          + -->
<!--   / \   / \     .-+-.   .-+-.     .+.     .+.      |   .--- 3      |   .-- 3   \ / 3 -->
<!--  /   \ /   \    |   |   |   |    |   |   |   |     '---+            '-+         + -->
<!--  1   2 3   4    1   2   3   4    1   2   3   4         '--- 4          '-- 4     \ 4 -->

<!-- ``` -->
<!-- ```goat -->
<!--    _________________ -->
<!--   ╱                 ╲                                                     ┌─────┐ -->
<!--  ╱ DO YOU UNDERSTAND ╲____________________________________________________│GOOD!│ -->
<!--  ╲ FLOW CHARTS?      ╱yes                                                 └──┬──┘ -->
<!--   ╲_________________╱                                                        │ -->
<!--            │no                                                               │ -->
<!--   _________▽_________                    ______________________              │ -->
<!--  ╱                   ╲                  ╱                      ╲    ┌────┐   │ -->
<!-- ╱ OKAY, YOU SEE THE   ╲________________╱ ... AND YOU CAN SEE    ╲___│GOOD│   │ -->
<!-- ╲ LINE LABELED 'YES'? ╱yes             ╲ THE ONES LABELED 'NO'? ╱yes└──┬─┘   │ -->
<!--  ╲___________________╱                  ╲______________________╱       │     │ -->
<!--            │no                                     │no                 │     │ -->
<!--    ________▽_________                     _________▽__________         │     │ -->
<!--   ╱                  ╲    ┌───────────┐  ╱                    ╲        │     │ -->
<!--  ╱ BUT YOU SEE THE    ╲___│WAIT, WHAT?│ ╱ BUT YOU JUST         ╲___    │     │ -->
<!--  ╲ ONES LABELED 'NO'? ╱yes└───────────┘ ╲ FOLLOWED THEM TWICE? ╱yes│   │     │ -->
<!--   ╲__________________╱                   ╲____________________╱    │   │     │ -->
<!--            │no                                     │no             │   │     │ -->
<!--        ┌───▽───┐                                   │               │   │     │ -->
<!--        │LISTEN.│                                   └───────┬───────┘   │     │ -->
<!--        └───┬───┘                                    ┌──────▽─────┐     │     │ -->
<!--      ┌─────▽────┐                                   │(THAT WASN'T│     │     │ -->
<!--      │I HATE YOU│                                   │A QUESTION) │     │     │ -->
<!--      └──────────┘                                   └──────┬─────┘     │     │ -->
<!--                                                       ┌────▽───┐       │     │ -->
<!--                                                       │SCREW IT│       │     │ -->
<!--                                                       └────┬───┘       │     │ -->
<!--                                                            └─────┬─────┘     │ -->
<!--                                                                  │           │ -->
<!--                                                                  └─────┬─────┘ -->
<!--                                                                ┌───────▽──────┐ -->
<!--                                                                │LET'S GO DRING│ -->
<!--                                                                └───────┬──────┘ -->
<!--                                                              ┌─────────▽─────────┐ -->
<!--                                                              │HEY, I SHOULD TRY  │ -->
<!--                                                              │INSTALLING FREEBSD!│ -->
<!--                                                              └───────────────────┘ -->
<!-- ``` -->
<!-- ```goat -->
<!-- ⎛1 2⎞   ⎛x⎞   ⎛1 ⋅ x + 2 ⋅ y⎞ -->
<!-- ⎜   ⎟ ⋅ ⎜ ⎟ = ⎜             ⎟ -->
<!-- ⎝3 4⎠   ⎝y⎠   ⎝3 ⋅ x + 4 ⋅ y⎠ -->
<!-- ``` -->
