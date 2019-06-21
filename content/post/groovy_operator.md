---
title: "Groovy Truth y nuevos operadores"
date: 2019-06-13T10:24:07-05:00
draft: false 
---
### Groovy truth

Continuando con groovy me encontré con una caracteristica muy interesante,**Groovy Truth**, es como se conoce a la capacidad que tiene groovy de extender la evaluación booleana de java. Dentro de una sentencia de decisión *if*  para poder evaluar si una cadena es vacia en java tendriamos que realizar algo similar a esto:
 
```java
	String strEmpty = "";
	if(strEmpty.isEmpty())
		System.out.println("cadena Vacia");
```

Donde se aprecia que es necesario llamar a un metodo que realice la evaluacion y de como resultado un valor booleano, ya que es el unico tipo de dato que puede evaliar java en una sentencia _if_  mientra que groovy 
ya evalua por defecto una cadena vacia como falso y no es necesario llamar a ningun metodo, otros elementos que groovy evalua como falsos por defectos son los que se aprecian en la imágen

![goovy_truth](/groovy_truth.png)

Esta simple pero conveniente aportación de groovy simplifica algunas de las validaciones mas comunes, 
por ejemplo, en ocasiones tendremos la necesidad validar si un elemento es distinto de **_null_** y al mismo tiempo que no sea un elemento **_vacio_**, para realizar esto bastaria con colocar el elemento en la sentencia _if_
y el resultado sera _true_ si cumple con ambos criterios.


### Nuevos operadores

Otra de las caracteristicas que llamo mi atención es la introducción de nuevos operadores como es el caso de **_Elvis("?.")_** el cúal es una interpretación distinta del operador ternario **?:** de java para la evaluación de una expresion boolena, elvis  hace uso de lo mencionado antes con groovy truth. 
El operador elvis esta pensado para que solo se realice una acción si el resultado de la operación boolena es falso, como el caso de la evalación de un elemento vacio, podriamos cambiar el estado del elemento si esté resulta estar vacio.

La comparación de elementos utilizado en diferentes escenarios cuando se esta desarrollando cualquier tipo de aplicación, por lo que existen distintos metodos para comparar estos elementos, en java contamos con compareTo() y equals() para hacer esta comparación siempre y cuando este implementada la interfaz comparable(). 
sin embargo groovy es capaz de realizar las llamadas a estos metodos infiriendolos usando simplement usando el operador **==**.

Sabiendo que se groovy hace uso de los metodos compareTo () y equals() por medio del operador **==**, entra en escena un nuevo operador que recibe el nombre de **_spacheship_**, este operador evalua 2 elementos y devueve un valor entero que puede ser 1 , -1 ó 0, dependiendo de los elementos a evaluar. 
Regresa un valor de 0 si los elementos son iguales, los valores 1 y -1 son devueltos en caso de que alguno de los operadores sea mayor que el otro de forma ascendente.
El valor 1 aplica cuando el operando de la izquierda es mayor al de la derecha y -1 en caso contrario, esto lo hace groovy de manera automatica gracias a las caracteristicas de los lenguajes dinamicos.

El ultimo operador que mencionare en este post es el denominado **_spreddot("*.")_**, dicho operador tiene una funcionalidad a los iterador de java para recorrer una coleccion de datos, pero de una manera mas concisa y sin requerir todos los pasos de crear un ciclo y pensar en una condicion de paro para poder obtener todos los elementos de una colección. También es muy util para la concatenación de colecciones ya va agregando elemento a elemento cuando es invocado.

Sigo encontrando caracteristicas interesantes en groovy y como es que hace mas digerible y amigable lo que ya se conoce se java pero sin complicar mucho las cosas al momento de realizar tareas sencillas.

