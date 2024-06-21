<h1 align="center"> :mortar_board:Actividad #3</h1>

<h2 align="center"> ⚠️Se debe seguir con la apliación que se hizo en el <a href="https://github.com/JuanJooose/Java_Course/blob/main/Tasks/Task_1.md">Task_1</a> </h2>

Antes de hacer la actividad debe de añadir las dependencia de SQL 

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

## La actividad deberá de tener:


* Entidades Users y Persons
* .
* Exception personalizada User.
* Controlador exception el cual ayuda a prevenir INTERNAL_SERVER_ERROR ó alguna exception.
* Método para agregar password a usuario.
* Método de login.
* Clase AppConfig que crea dos listas( Una lista con usuarios sin contraseña y viceversa ).

