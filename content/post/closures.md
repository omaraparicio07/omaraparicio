---
title: "¿Que son los closures?"
date: 2019-06-14T16:17:02-05:00
draft: false 
---

Dentro de los elementos mas complicados de digerir hasta el momento en groovy es el concepto de closures, el había tenido un acercamiento trabajando con javascript pero no tenía idea de que recibiera ese nombre. Tratando de relacionarlos, los callbacks de js tiene un comportamiento similar a los closures aunque no se si tengan el mismo alcance, me explico, 
por lo que he estado checando los closures de groovy permiten realizar acciones y retornar un valor hasta aqui es identico a un callback de js pero groovy tiene la capacidad de delegar acciones que se ejecuten fuera del propio alcance del closure y con js no se si se pueda realizar este tipo de comportamiento.
 

### Closures

Antes que nada debo mencionar que es un closure o como es que yo lo entiendo, en terminos simples es un fragmento de codigo que se envuelve en un objeto y este objeto puede o no recibir parametros y retornara siempre un valor. 
Los closures tiene una funcionalidad similar a los apuntadores a funciones del lenguaje C pero tratando todo como un objeto y 
haciendo uso del tipado dinamico de los lenguajes dinamicos, esta ultima caracteristica puede ser conflictiva ya que en un proyecto bien estructurado seria una buena practica definir el tipo de dato que recibira un closure 
, aunque los tipados dinamos son utiles en ciertos caso tambien es importante la validación de los tipos de dato estaticos sobre todo para hacer la aplicación resistente a fallos.


Los closures tienen multiples usos, uno de los mas comunes es el manejo de estos para trabajar con el manejo de colecciones como pueden ser listas o mapas en groovy. 
Algo importante para poder sacar mayor provecho de los closures en groovy es tener presente que si un metodo recibe como ultimo parametro un closure, este puede ser excluido de la lista de parametros que recibe el metodo y mandar la definicion del closure inmediatamente seguido de la llamada a la funcion envolviendolo con las llaves **_{ }_**.

En la imagen se puede apreciar las distintas formas para llamar a un closure:

![cloruse como ultimo parametro ](/closure_params.png)

poder pasarle un closure  a un metodo es algo de mucha utilidad y es com funcionan algunas de las funciones que en algun momento usamos sin saber, por ejemplo, iterar una lista de elementos con la función **_each_**, este metodo recibe un closure como ultimo parametro por ello es que ejecuta las acciones que nosotros defimos en dentro de las llaves al llamar al metodo, lo que me queda en duda es si existe una convención establecida de cuando un closure es demasiado grande y es recomendable separarlo en otros closure o metodos.

### Delegación de un closure 

Todo closure tiene 3 propiedades que nos ayudan a conocer quien esta llamando al closure, estas propiedades son:

**this**:

esta propiedad hacer referencia al contexto donde esta definido el closure, es parecido al this de java. Es decir que this hace referencia a la intancia de la clase que contiene al closure.

**owner**

hace referencia al elemento que esta llamando al closure, puede ser el mismo que _'this'_, pero cambia si la llamada al closure se realiza dentro de otro closure, es decir si se encuentra anidado.

**delegate**

normalmente toma el mismo valor que owner, pero puede ser cambiado si es que se requiere que ejecute acciones en otro localidad distinta al contexto actual, esta propiedad de los closures toma mayor importancia cuando se esta trabajando con meteprogramación de groovy, un tema mucho mas complejo y que no se tocara en este post y probablemente en blog.



