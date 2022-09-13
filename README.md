# consultas1_sql

# EJERCICIOS CONSULTAS SQL

## Tabla usuario

![tabla usuario](img/tabla_usuario.png "Tabla usuario")

1. Para visualizar toda la información que contiene la tabla `usuario` se puede incluir con la instrucción SELECT el caracter `^` o cada una de los campos de la tabla 

`select * from usuario`

![Consulta1](img/consulta1.png "Consulta1")


2. Seleccionar o visualizar solamente la identificación del usuario.

`select identificación from usuario`

![Consulta2](img/consulta2.png "Consulta2")

3. Si se desea optener los registros cuya identificación mayor o iguales a 150, se debe utilizar la clausura WHERE que especifica las condiciones que debe reunir los registros que se van a seleccionar.

`SELECT * FROM usuario WHERE identificación>=`150``

![Consulta3](img/consulta3.png "Consulta3")