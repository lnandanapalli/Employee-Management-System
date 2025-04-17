# Employee Management System

A Spring Boot MVC application for employee management.  
Technology stack: **Java 17**, **Spring Boot 3**, **Spring Data JPA**, **Thymeleaf**, **MySQL**, **Maven**.

---

## Features

-   List employees with pagination and sorting
-   Add, update, and delete employee records
-   Thymeleaf templates for server-side rendering
-   Spring Data JPA repository layer

---

## Prerequisites

| Tool  | Version      |
| ----- | ------------ |
| JDK   | 17 or newer  |
| Maven | 3.6+         |
| MySQL | 8.x (or 5.7) |

---

## Setup

1.  **Create a database**

        CREATE DATABASE ems;

2.  **Configure credentials**  
    Edit `src/main/resources/application.properties`:

         spring.datasource.url=jdbc:mysql://localhost:3306/ems
         spring.datasource.username=<your-user>
         spring.datasource.password=<your-password>

3.  **Build and run**

         mvn spring-boot:run

    The application starts on <http://localhost:8080/>.

---

## Project structure

        src
         |-- main
             |-- java/com/example/ems
             |   -- controller      MVC controllers
             |   -- model           JPA entities
             |   -- repository      Spring Data repositories
             |   -- service         Service layer
             |-- resources
                 -- templates       Thymeleaf views
                 -- application.properties

---

## Endpoints

| Method | Path                      | Purpose              |
| ------ | ------------------------- | -------------------- |
| GET    | `/`                       | Employee list        |
| GET    | `/showNewEmployeeForm`    | Add-employee view    |
| POST   | `/saveEmployee`           | Persist new employee |
| GET    | `/showFormForUpdate/{id}` | Edit-employee view   |
| GET    | `/deleteEmployee/{id}`    | Delete employee      |

---

## Running tests

        mvn test
