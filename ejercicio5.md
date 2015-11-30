# Ejercicio 5

Elimine el direcotorio de datos de su servidor mongo  
Inicialize una instancia mongod con un nuevo directorio de datos

## mongoImport y mongoExport

Utilizando mongoimport cargue el archivo zips.json en la base de datos zipsdb, en la colección zips.  
Utilizando mongoexport, exporte la colección zips en los formatos JSON, CSV y TSV.  
Tome alguno de los formatos exportados y utilizando algún editor de texto de su preferencia cambie todos los registros al estado de "AL".  
Import esta colección en la colección zipsal utilizando mongoimport. 
Utilizando la opción --upsert actualice toda la colección zips. Compruebe que ahora todos los registros corresponde al estado "AL".  


## mongodump y mongorestore

Cree ahora un backup de la base de datos zips utilizando el comando mongodump.  
Elimine el direcotorio de datos de su servidor mongo  
Inicialize una instancia mongod con un nuevo directorio de datos.  
Utilizando el comando mongorestore restaure el backup.  
Compruebe que la base de datos fue restaurada.  



