# Ejercicio 4



## Replica Set
 * Cree un replica set denominado "mireplica". El replica set debe estar compuesto por un primario y dos secundarios
 * En el primario, cree una base de datos llamada futbol, y una colección llamada jugadores. Inserte al menos unos 10 jugadores (Puede ser solo el campo nombre)
 * Confirme que al insertar los jugadores estos son replicados hacia los nodos secundarios
 * Conectese al nodo primario y haga un shutdown. Verifique cual nodo queda como primario
 * Vuelva a iniciar al ex-nodo primario que bajó en el paso anterior y comprueba que ahora asume como nodo secundario.
 * Obtenga la configuracion  del replica set y cambie un de los 2 miembros secundarios a Arbitro. Indicación: Para ello debe cambiar el campo  arbiterOnly a true en uno de los dos miembros.
 
 
## Sharding
 
 * Cree un shard compuesto por un nodo Config, un Router y tres Shard pero sin réplica
 * En el Router, cree una base de datos llamada futbol, y una colección llamada jugadores. Inserte al menos unos 100000 jugadores  ocupando un ciclo for
 * Una vez insertados los jugadores confirme que fueron distribuidos hacia los shards, ocupando el comando sh.status()
 
## Backup y Restore
 
 * Realice un backup  de la base de datos zipsdb
 * Elimine el direcotrio de datos cree uno nuevo vacío
 * Restaure la base de datos.
 
 
 
 
 