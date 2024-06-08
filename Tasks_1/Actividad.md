<h1 align="center"> :mortar_board:Actividad #1</h1>

El programa hecho en Java Spring boot, deberá de tener este controlador, Utilizar las dependecias Spring web, devtools and actuator,

La actividadd deberá de tener:

* Modelo users con: id,name y lastname
* Services 
* Repositorys
* Mostrar datos
* Cambiar nombre de x user
* agregar user

Son libres de utilizar cualquier parámetro para obtener los datos y hacer los respectivos procesos. 
Se recomienda utilizar @RequestParam

La solución de la actividad se deberá presentar en Postman.


Adjunto pista/base de como deberia de ser el controlador (le faltan cosas que se lo dejo a sus disposición). 
```java, package com.activity.one.course.task_one.Controllers;

import java.util.List;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

import com.activity.one.course.task_one.Models.Users;
import com.activity.one.course.task_one.Services.UsersService;

@RestController
@RequestMapping("api")
public class UsersController {

    @Autowired
    private UsersService service;

    @GetMapping({"**", "", "home"})
    public List<Users> home() {
        // Code ...
    }

    @PostMapping("change-name")
    public List<Users> changeName() {
        // Code ...
    }

    @PostMapping("create")
    public List<Users> create() {
        // code..;
    }

}
```
