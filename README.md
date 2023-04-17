# JavaFullStack

Java fullstack CRUD application
Fullstack Java applicaion with API and a MySQL database, frontend written in react

Only funtion is to demonstrate CRUD functionality

This program is a simple student management system built using Spring Boot, a widely used Java framework for building web applications. It allows you to add new students and retrieve a list of all students. The application is organized into four main packages: controller, model, repository, and service. Each package has a specific purpose and responsibility.

Controller (StudentController.java):
This class is responsible for handling incoming HTTP requests and mapping them to the appropriate methods. It uses annotations like @RestController, @RequestMapping, and @CrossOrigin to define its behavior. The @Autowired annotation injects the StudentService dependency.
@PostMapping("/add"): Maps the "/add" POST request to the add method, which takes a Student object as input and adds it to the database.
@GetMapping("/getAll"): Maps the "/getAll" GET request to the list method, which returns a list of all students.
Model (Student.java):
This class represents the Student entity and its attributes (id, name, and address). It uses the @Entity annotation to mark it as a database entity and the @Id and @GeneratedValue annotations to define the primary key and its generation strategy.

Repository (StudentRepository.java):
This interface extends JpaRepository and provides methods for performing CRUD (Create, Read, Update, Delete) operations on the Student entity. The @Repository annotation marks it as a Spring Data JPA repository.

Service (StudentService.java and StudentServiceImpl.java):
The StudentService interface defines the methods that the service layer should implement. The StudentServiceImpl class provides the actual implementation of these methods. The @Service annotation marks this class as a service, and the @Autowired annotation injects the StudentRepository dependency.

saveStudent(Student student): Saves a new student to the database.
getAllStudents(): Retrieves a list of all students.
Libraries used:

Spring Boot: Provides the foundation for building Java-based web applications.
Spring Data JPA: Simplifies database access and reduces boilerplate code by providing a layer of abstraction over the Java Persistence API (JPA).
Spring Web: Includes the Spring MVC framework and provides functionality for building web applications with Spring.
javax.persistence: Provides the Java Persistence API, a standard for ORM (Object-Relational Mapping) in Java.
In summary, the program provides a simple API to manage students using the Spring Boot framework. It includes a controller for handling HTTP requests, a model for representing the student entity, a repository for database operations, and a service layer for implementing business logic.