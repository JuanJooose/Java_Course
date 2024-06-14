<h1 align="center"> :mortar_board:Actividad #2</h1>

<h2 align="center"> ⚠️Se debe seguir con la apliación que se hizo en el <a href="https://github.com/JuanJooose/Java_Course/blob/main/Tasks/Task_1.md">Task_1</a> </h2>

### La actividad deberá de tener:

* Modelo users con: id, name, lastname y password.
* Modelo Exception con sus respectivas variables.
* Exception personalizada User.
* Controlador exception el cual ayuda a prevenir INTERNAL_SERVER_ERROR ó alguna exception.
* Método para agregar password a usuario.
* Método de login.
* Clase AppConfig que crea dos listas( Una lista con usuarios sin contraseña y viceversa ).


## ⚠️Las listas se utilizarán para probar los métodos nuevos.

Son libres de utilizar cualquier parámetro para obtener los datos y hacer los respectivos procesos.

Se recomienda utilizar <h3> @RequestParam. </h3> 

# ¿Qué debo presentar?

## En Postman.

- Cambiar la contraseña y, con este cambio hecho, iniciar sesión.
- iniciar sesión validando si el usuario y contraseña existen en la bd (Lista).

Adjunto pista/base de como deberia de ser el controlador (le faltan cosas que se dejan a su disposición). 
```java,
package com.activity.one.course.task_one.Controllers;

import java.util.List;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

import com.activity.one.course.task_one.Exceptions.UserExceptions;
import com.activity.one.course.task_one.Models.Domains.Users;
import com.activity.one.course.task_one.Services.UsersService;

@RestController
@RequestMapping("api")
public class UsersController {

    @Autowired
    private UsersService service;
    
    @GetMapping({"**", "", "home"})
    public List<Users> home() {
        return service.findAll();
    }

    @PostMapping("change-name")
    public List<Users> changeName(@RequestParam Long id, @RequestParam String name) {
        return service.nameChanger(name, id);
    }

    @PostMapping("create")
    public List<Users> create(@RequestParam String name, @RequestParam String lastname) {
        return service.addUser(name, lastname);
    }

    @PostMapping("login") 
    public String login(@RequestParam String name, @RequestParam String password) {
       ...
    }

    @PostMapping("new-password")
    public String newPassword(@RequestParam String newpassword,@RequestParam Long id) {
        ...
    }
}
```
