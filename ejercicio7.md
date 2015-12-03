# Ejercicio 7

Cree un usuario root

Cree una base de datos llamada seguridad.  
En esa base de datos agregue un usuario administrador.  
A continuación cree una colección llamada alumnos en la base  de datos curso. 

Recuerde iniciar el demonio mongod con la opción --auth 

## usuarios

  * Cree un usuario llamado lectura con password lectura123, con privilegios de find para la colección curso
  * Desconectese de mongoshell y vuelva a conectarse como el usuario lectura. Comprueba que no puede insertar datos en la colección alumnos.
   * Cree un usuario llamado insertar con password insertar123, con privilegios de find e insert para la colección curso
  * Desconectese de mongoshell y vuelva  a conectarse como el usuario insertar. Comprueba que puede insertar datos en la colección alumnos, pero que no puede realizar updates ni borrar.
    * Cree un usuario llamado full con password fullrw123, con privilegios de find, insert, update y remove para la colección curso
  * Desconectese de mongoshell y vuelva a conectarse como el usuario full. Compruebe que realizar todas las operaciones sobre la colección alumnos.
  
  
Ejecute el comando getUsers() y/o getUser() para obtener los usuarios 

## roles

  * Cree un rol llamado lecturarol con privilegios de find para la colección curso
  * Elimine el usuario lectura creado en el ejercicio anterior y vuelva a crearlo pero ahora asignandole el rol lecturarol (Password lectura123)
  * Desconectese de mongoshell y vuelva a conectarse como el usuario lectura. Comprueba que no puede insertar datos en la colección alumnos.
  * Cree un rol llamado insertarrol  con privilegios de find e insert para la colección curso
  * Elimine el usuario insertar creado en el ejercicio anterior y vuelva a crearlo pero ahora asignandole el rol insertarrol (Password insertar123)
  * Desconectese de mongoshell y vuelva  a conectarse como el usuario insertar. Comprueba que puede insertar datos en la colección alumnos, pero que no puede realizar updates ni borrar.
  * Cree un rol llamado fullrol, con privilegios de find, insert, update y remove para la colección curso
  * Elimine el usuario full creado en el ejercicio anterior y vuelva a crearlo pero ahora asignandole el rol fullrol (Password fullrw123)
  * Desconectese de mongoshell y vuelva a conectarse como el usuario full. Compruebe que realizar todas las operaciones sobre la colección alumnos.
  
  
Ejecute el comando getUsers() y/o getUser() para obtener los usuarios 
Ejecute el comando getRoles() y/o getRol() para obtener los usuarios 

  
  
  