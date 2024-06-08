<h1 align="center"> :mortar_board:Actividad #1</h1>

El programa hecho en Java Spring boot, deberá de tener este controlador


```java, package com.activity.one.course.task_one.Controllers;

import java.util.List;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
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

}
```
