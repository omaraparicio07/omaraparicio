---
title: "Iniciando con groovy"
date: 2019-06-12T08:50:47-05:00
draft: true
---
Trabajando con anterioridad con el lenguaje java empezabá a pensar que entre mas tecnologías de dicho lenguaje aprendiera sería cada vez más complicado recordar la sintaxis, decoradores, estructuras que maneja cada una de ellas. El simple hecho de no olvidar colocar el nivel de acceso a un metodo o atributo se vulve algo tedioso en un proyecto con una cantidad de elementos.

Hace poco me enteró que existe una alternativa a java llamada groovy, un lenguaje que también es ssoportado por la JVM(Java Virtual Machine) y que es capaz de ejecutar todo codigo escrito en java sin realizar ningún cambio. Groovy es visto como una version mejorada de java por  varias razones, entre ellas las que más me llamaron la atención son: 

-**Sintaxís simple**

Goovy poseé una sintaxis sencilla parecida a lenguajes como python o pearl,lo cual reduce la dificultad al escribir codigo y facilita mantener proyectos grandes. El tipado dinamico de estos lenguajes es una caracteristica que también se encuentra presente en groovy, esta sencilla caracteristica reduce la complejidad para el desarrollador.

-**Dualidad con java** 

Todo lo que ya este realizado en java puede ser utilizado en groovy y viceversa, podemos extender las capacidades de un proyecto completo escrito en java y no requerimos de cambiar todo el codigo ya escrito y probado a la sintaxis de groovy. Se puede resumir a la siguiente frase "si funciona en java funciona en groovy".

-**Obviedad de algunos elementos**

Como complemento a la sintaxis simple de groovy se añade la caracteristica que se pueden "obviar" u "omitir" ciertos elementos que hacen de java algo tedioso al escribir un codigo simple. Dentro de estos elementos se encuentra el presindor de los ';' para terminar una sentencia.

Los niveles de acceso como ya mencione son opcionales, si en un momento no declaramos el metodo de accesso en algun atributo o metodo groovy asumira que es plublico, no tenemos la necesidad de declarar metodos de acceso a los atributos (getter y setter) ya que seran generados en tiempo de ejecución. De los elementos mas interesantes que se pueden obviar en groovy es el  ***return*** de un metodo ya que al ser ejecutado un archivo groovy este regresa siempre el ultimo elemento que haya sido evaluado. 

Como indica el titulo este post solo expresa mi primera impresión con groovy, seguire trabajando con el lenguaje y expandir el panorama de proximos post y compartir mi experiencia con nuevos descubrumiento u obstaculos que encuentre.
