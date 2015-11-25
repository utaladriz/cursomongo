# Ejercicio 3

* Utilice la base de datos zipsdb y la colección zips
* Obtenga la población total del estado de California (CA)
* Obtenga la población total de la ciudad de New York
* Considerando el siguiente ejemplo que devuelve los estados cuya  población supera los 10.000.000


```
db.zips.aggregate( [
   { $group: { _id: "$state", totalPop: { $sum: "$pop" } } },
   { $match: { totalPop: { $gte: 10*1000*1000 } } }
] )
```

Realice una consulta que permita obtener estados cuya población no supere los 2.000.000 de habitantes

 * Pruebe la siguiente consulta que calcule el promedio de habitantes por ciudad y estado
 
 ```
 db.zips.aggregate( [
   { $group: { _id: { state: "$state", city: "$city" }, pop: { $sum: "$pop" } } },
   { $group: { _id: "$_id.state", avgCityPop: { $avg: "$pop" } } }
] )
```

* Pruebe la siguiente consulta que permite obtener las ciudades con menor y mayor población por estado
 
 ```
db.zips.aggregate( [
   { $group:
      {
        _id: { state: "$state", city: "$city" },
        pop: { $sum: "$pop" }
      }
   },
   { $sort: { pop: 1 } },
   { $group:
      {
        _id : "$_id.state",
        biggestCity:  { $last: "$_id.city" },
        biggestPop:   { $last: "$pop" },
        smallestCity: { $first: "$_id.city" },
        smallestPop:  { $first: "$pop" }
      }
   },

  // the following $project is optional, and
  // modifies the output format.

  { $project:
    { _id: 0,
      state: "$_id",
      biggestCity:  { name: "$biggestCity",  pop: "$biggestPop" },
      smallestCity: { name: "$smallestCity", pop: "$smallestPop" }
    }
  }
] )
 ```
 
 * Aplicando map reduce obtenga la población total del estado de California (CA)
 * Aplicando map reduce obtenga la población total de la ciudad de New York