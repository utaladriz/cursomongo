# Ejercicio 2

## Modelamiento

En este ejercicio vamos a modelar la estructura de un sitio de noticias. Recuerde que en mongoDB no existen los esquemas, por lo que para reflejar el modelo pensado, deberá crear documentos en distintas colecciones. Cree una base de datos nueva para el modelo.

## Problema

El diario "El Hocicón", diario pobre pero honrado, ha decidido renovar su sitio de noticias, y para ello está evaluando utilizar mongoDB y le ha solicitado mostrar las bondades de mongoDB, a través de un modelamiento de sus necesidades  

La problemática de "El Hocicón" es la siguiente:  

* Las noticias son creadas por periodistas
* Las noticias son revisadas por un editor que las publica
* Cada noticia tiene un título, una bajada y un texto completo. Además tiene la fecha de publicación y los tags para clasificarla. El editor asigna la sección donde se publica la noticia, que pueden ser Nacional,Internacional, Deportes, Farándula y Economía. Las noticias se publican en solo una sección
* Es muy importante para "El Hocicón" saber cuantas personas ha "visto" la noticia
* Una "Edición" agrupa todas las noticias publicadas en la fecha que corresponde a la edición
* Para los colaboradores del diario, periodista y editores, es importante tener su información personal, como Nombre completo, dirección y datos de contacto. Esto último es muy importante porque en el caso de los periodistas deben ser "ubicables" para cubrir las noticias en terreno.  
* Las noticias publicadas incluyen el nombre del periodista que la redactó al momento de mostarlas en el sitio.
* Los usuarios registrados pueden publicar comentarios en las noticias
* Los usuarios registrados tienen un nombre de usuario, un email y una clave
* "El Hocicón" se financia a través de los anuncios. Cada anuncio tiene una fecha de inicio de publicación y de término de publicación. Es importante contar cada vez que el anuncio se muestra en el sitio.
* Un motor de anuncios, que no es parte del problema, determina que anuncio mostrar y en cual notica. Si es parte del problema que se le pide solucionar registrar la información de cuales anuncios se han mostrado con una noticia dada.



