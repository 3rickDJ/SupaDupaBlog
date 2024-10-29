---
title: "BlockChain"
date: 2023-09-06
description: "Qué es el blockchain, qué es un nft, cómo funcionan, cómo me puedo beneficiar, por qué debería de aprenderlo"
summary: "En mi trabajo surgió un nuevo proyecto de boletos con blockchain y nft's. Idea de Jorge Sanchez. Este es el inicio donde no tenía claro que era un blockchain, y aún no tengo claro que es un nft. Todos hemos escuchado Non-Foundable-Token... Pero a qué se refiere y por qué me debería de importar"
draft: true
categories: ["blockchain", "block-chain", "nft", "non foundable token", "crypto"]
tags: [""]
keywords: [""]

---

# BlockChain

Realicé una pequeña búsqueda sobre lo que es el blockchain. Resulta ser una tecnología, una estructura de datos para ser más específico. Esta estructura de datos es un compendio de tecnologías que datan de muchos años (hace 30 años se inventó las tablas hash) que en conjunto propician una plataforma para hacer registros de forma segura, descentralizada y anónimamente pública. Realmente este auge del blockchain inició en el #### cuando Satoshi Nakamoto (una persona, organización o grupo de personas) liberaron al mundo un paper sobre una nueva forma de economía digital. Ya que ellos, él proponía que presindieramos de un ente central para resolver el problema del doble gasto (este problema surge cuando una persona tiene x cantidad de dinero y a alguien le paga $x por un plátano y a otra persona $x por una manzana, cómo es que los compradores pueden estar seguros que no "duplicó" su dinero a gusto y que en realidad tenía suficientes fondos para pagar y se le descontaron de su saldo). La forma que encontraron es bastante curiosa.

1. Inician por establecer una estructura de datos que se vea compuesta por bloques o elementos
2. Estos elementos contienen las transacciones efectuadas, un identificador único del bloque/elemento anterior, un identificador de todos los bloques anteriores (esto la hace una cadena ligada a su historia anterior, dotándola de una gran dificultad para modificarla) y otro número especial
3. Las nuevas transacciones efectuadas se hacen agregándolas en bloques nuevos y ligándolas a la cadena de bloques

Pero nos preguntamos por qué es distribuida, pues esto es porque no necesita de un ente central regulador como un banco que tenga a su disposición todos los datos de los cuentahabientes y de cada una de las transacciones que se hacen. Más específicamente es una red de nodos en el que cada nodo es un participador de la red. Y como participadores de la red cada nodo tiene una copia de toda la blockchain, o en otras palabras tiene una copia de todas las transacciones que se han hecho en la blockchain.

Pero cómo es que un nodo participante hace una transacción. Esta transacción la hace y la envía a los demás nodos (no tiene por qué llegar a todos, solo a suficientes para que lo capture un nodo que registra). Te imaginarás que sin una entidad central cualquiera pudiese modificar lo que va a enviar o recibir, pero esto no es del todo cierto. Pues ya que todos los nodos tienen acceso a las transacciones de cada quien, cada nodo puede verificar si la transacción es válida y aceptar o no y rechazarla.

Ahora te preguntarás si verifican las transacciones, por qué no solo modifican el historial de las transacciones (modificar o sustituir un bloque). Y es que esto no es del todo fácil ya que para que un bloque sea aceptado no solo hace falta que todas las transacciones sean válidas. Pues muchos nodos pueden contener bloques con transacciones diferentes o iguales pero en distinto orden. Aún así todas estas transacciones pueden ser válidas. Nos encontramos con un problema de tener nuestro sistema distribuido y este es el problema de consenso. Cómo consentimos qué bloque debería ser el siguiente en la cadena de bloques. Pues para solucionar este problema se recurre a una estrategia de consenso llamada Proof of Work (prueba de trabajo). Esta prueba evitará que alguien se pueda hacer pasar por muchas computadoras y votar por un determinado bloque. Este bloque deberá de ser modificado (sin alterar el contenidode las transacciones, la prueba de trabja consiste en encontar un número tal que si se obtiene el hash del bloque anterior y este has empieza con 7 ceros,

##
