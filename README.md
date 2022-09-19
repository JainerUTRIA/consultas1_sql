# consultas1_sql

# EJERCICIOS CONSULTAS SQL

## Tabla usuario

![tabla usuario](img/tabla_usuario.png "Tabla usuario")

## COMANDO SELECT

1. Para visualizar toda la información que contiene la tabla `usuario` se puede incluir con la instrucción SELECT el caracter `^` o cada una de los campos de la tabla 

`select * from usuario`

![Consulta1](img/consulta1.png "Consulta1")


2. Seleccionar o visualizar solamente la identificación del usuario.

`select identificación from usuario`

![Consulta2](img/consulta2.png "Consulta2")

3. Si se desea optener los registros cuya identificación mayor o iguales a 150, se debe utilizar la clausura WHERE que especifica las condiciones que debe reunir los registros que se van a seleccionar.

`SELECT * FROM usuario WHERE identificación>=`150``

![Consulta3](img/consulta3.png "Consulta3")

4. Si se desea obtener los registros cuyos apellidos sean Vanegas o Cetina, se debe utilizar el operador IN que especifica los registros que se quieren visualizar de una tabla.

`SELECT apellidos FROM usuario WHERE apellidos IN (`Vanegas`,`Cetina`)`

![Consulta4](img/consulta4.png "Consulta4")

`SELECT apellidos FROM usuario WHERE apellidos=`Vanegas`OR apellidos=`Cetina``

![Consulta4.2](img/consulta4.2.png "Consulta4.2")


5. Si se desea obtener los registros cuya identificación sea menor de '110' y la ciudad sea 'Cali', se debe utilizar el operador AND.

`SELECT * FROM  usuario WHERE identificacion<'110' AND ciudad_nac='Cali'`

![Consulta5](img/consulta5.png "Consulta5")

6. Si se desea obtener los registros cuyos nombres empiecen por la letra 'A', se debe utilizar el operador LIKE que utiliza los patrones'%' (todos) y '_' (caracter).

`SELECT * FROM usuario WHERE nombre LIKE 'AN'`

![Consulta6](img/consulta6.png "Consulta6")

7. Si desea obtener los registros cuyos nombres cotengan la letra 'a'.

`SELECT * FROM usuario WHERE nombre LIKE '%a%'`

![Consulta7](img/consulta7.png "Consulta7")

8. Si se desea optener los registros donde la cuarta letra del nombre sea una 'a'.

`SELECT * FROM usuario WHERE nombre LIKE '___a%'`

![Consulta8](img/consulta8.png "Consulta8")

9. Si se desea obtener los registros cuya ientificación esté entre el intervalo 110  y 150, se debe utitilizar la cláusula BETWEEN, que sirve para especificar un intervalo de valores.

`SELECT * FROM usuario WHERE identificación BETWEEN '110' AND '150'`

![Consulta9](img/consulta9.png "Consulta9")



## COMANDO DELETE

10. Para eliminar solamente los registros cuya identificación sea mayor a 130.

`DELETE FROM usuario WHERE identificacion>'130'`

![Consulta10](img/consulta10.png "Consulta10")
![Consulta10](img/consulta10_2.png "Consulta10")


## COMANDO UPDATE

11. Para actualiar la ciudad de nacimiento de Cristian Vanegas, cuya identificacion es 114.

`UPDATE usuario SET ciudad_nac = 'Manizales' WHERE identificación='114'`

![Consulta11](img/consulta11.png "Consulta11")



## INNER JOIN

Permite obtener datos de dos o mas tablas. Cuando se realiza la concatenación de las tablas, no necesariamente se deben mostrar todos los datos de las tablas.

## Tabla pedidos 

![Tabla pedidos](img/Captura%20de%20pantalla%20de%202022-09-19%2016-26-58.png  "tabla pedidos")

12. Para visualizar los campos identificacion, nombre, apellidos de la tabla usuario y nropedido, fecha de compra, fecha de vencimiento y observacion de la tabla pedidos, se debe realizar la siguiente instrucción SQL: 

´SELECT usuario.identifiacion, usuario.nombre, usuario.apellido, pedidos.nrpedidos, pedidos.fecha compra, pedidos.fechaVence, pedidos.observación FROM usuarios INNER JOIN pedidos ON usuario.identificacion = pedidos.identifiacion´

![Consulta12](img/consulta12.png "Consulta12")