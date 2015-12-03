# Ejercicio 8

## Prompt

Cambie el prompt de mongo shel a su nombre y el tiempo de uptime del servidor
Para ello modifique el archivo .mongorc.js

## Funciones 1

Use la base de datos ejercicio8

Cree una colección que incluya dos campos. Un campo llamado nombre de tipo string y otro campo llamado amigos, que es un arreglo de nombres (Strings) con los amigos de la persona.  


Cree primero una función que reciba un arreglo que devuelva una valor verdadero si es que el arreglo contiene más de 3 elementos.  

Pruebe esta funcion invocandola desde el shell mongo. Por ejemplo

> tiene3(["Luis"],["Pedro"],["Jorge"])  
> true

Luego Agregue esta función a las funciones del sistema

Luego agregue una función que partir de un documento que se reciba como parámetro devuelva verdadero si el documento tiene un campo amigos y este es un arreglo de largo igual o mayor a 3 (Hint use Array.isArray())

Agregue esta función al sistema  

Cree ahora una consulta $where utilizando la última función guardada

## Funciones 2

Agregue un usuario read write a la base de datos zipsdb  
Inicie  mongod en modo de autenticación
Cree un script js para ser ejecutado desde mongo shell que se conecte a la base de datos (desde el código )utilizando el usuario read-write y que devuelva por cada locación un String con el siguiente formato:  
(ciudad:"Nombre de la ciudad", estado:"Nombre del estado")

Pruebe su script con mongo nombrescript.js

Modifique el script ahora para invocar la función creada en el último paso de funciones 1 y con esto lograr la salida:


(ciudad:"Nombre de la ciudad", estado:"Nombre del estado", amigos : false)

