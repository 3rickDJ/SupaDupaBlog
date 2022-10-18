---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date | time.Format ":date_long" }}
description: "Place here your description"
categories:
draft: true
cover:
    image: 'img/sketchAnimation.png'
    alt: 'this is a post image'
    caption: 'close caption?'
categories: ["Example"]
tags: ["Down", "Goooo"]
keywords: ["One",]

---

# {{ replace .Name "-" " "}}

## Sub
