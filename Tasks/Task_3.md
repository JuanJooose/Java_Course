<h1 align="center"> :mortar_board:Actividad #3</h1>

<h2 align="center"> ⚠️Se debe seguir con la apliación que se hizo en el <a href="https://github.com/JuanJooose/Java_Course/blob/main/Tasks/Task_1.md">Task_1</a> </h2>

El controlador ahora se pasa a llamar AdminController o crean uno nuevo. Está a su disposición.

Antes de hacer la actividad debe de añadir las dependencia de MySQL.

```xml,
<dependency>
			<groupId>com.mysql</groupId>
			<artifactId>mysql-connector-j</artifactId>
			<scope>runtime</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>

```

* Crear entidades Users y Persons

Supongamos que usted es el adminitrador de x empresa y desea hacer las siguientes acciones.

## Acciones:

* Cambiar usernanme, password, name, lastname de las personas. 
* Login.
* Ver las personas con sus respectivos usuarios.
* Eliminar personas (debe de eliminar la persona como también su usuario).

Todo esto el adminitrador lo puede ver mediante Postman.

