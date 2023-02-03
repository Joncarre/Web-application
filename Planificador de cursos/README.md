<!--Creado por Jonathan Carrero Aranda -->

**Course scheduler**
==============
----------
     
In this small project we implement a very basic web application to manage classroom courses of various kinds: programming, cooking, dance, music, etc.. The server will contain a database with available courses. The users of the application can search for a specific course by its name and register in one or more courses.

## Competencies and implementation
---------------------------

The main objective is the implementation of REST APIs and the development of a web application using AJAX and the SPA model.
A SPA (*Single Page Application*) is a web application contained in a single HTML document. The components of this document are shown or hidden as the user interacts with the web application.

Emphasis is also placed on the correct design of the RESTful API and its implementation in *Express.js*. On the other hand, the server works through the HTTPS protocol.

We have made use of technologies such as Bootstrap to facilitate the positioning of the elements and relational databases with *MySQL* managed through *PhpMyAdmin*.

## Summary of the project structure by folder
---------------------------

**Helpers:** set of methods that help to form the view and that, for the most part, are common to most of the project.

**integration:** here are stored the Data Access Objects that retrieve and insert information to the database (as they are in the integration layer).

**nbproject:** internal files used by *NetBeans* (IDE used for the development of the application).

**node_modules:** modules used by *Node* (server side).

**public:** here are the public files of the project, that is to say, those necessary resources that are directly exposed to the client. Some of the files contained are: the *index* page, libraries like jQuery, the CSS of the application, used images, etc.

**routes:** routers container. A route is like a mini-web application with its own routes and its own middleware chain. In this case, we only have two routers: users and courses.

The rest of the files contain information about the project (.json), the database used (.sql), the certification for the use of the HTTPS protocol or the entry point in the application execution flow (app.js).

## Basic user guide
----------------------

When you enter the planner you can consult the available courses without having to be registered. However, if what we want is to have a good organization and to be able to enroll in the courses, then it is necessary to have an account.

When we search for courses, this search performs a check in the database and shows all the courses that contain, in their title, the searched string. For example, if we search for *cooking*, all the results that contain that word will appear.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Planificador%20de%20cursos/images/imagen1.png)

If we click on a course we can see information about it, but as it is logical, it will not let us register until we are not registered.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Planificador%20de%20cursos/images/imagen2.png)

Once registered, we can start creating courses that may be of interest to other users of the application. In addition, the system organizes the courses in such a way that it is easy for the user to consult the courses they have already completed, the ones they are currently taking and what timetable they have set for each week.

![enter image description here](https://github.com/Joncarre/Programacion-web/blob/master/Planificador%20de%20cursos/images/imagen3.png)
