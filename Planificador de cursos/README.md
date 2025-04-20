<!--Creado por Jonathan Carrero Aranda -->

**Course Scheduler** 📅
==============
----------
     
In this small project, we implement a very basic web application to manage classroom courses of various kinds: programming 💻, cooking 🍳, dance 💃, music 🎵, etc. The server contains a database with available courses. Users can search for specific courses by name and register for one or more courses.

## Competencies and implementation 🛠️
---------------------------

The main objective is the implementation of REST APIs and the development of a web application using AJAX and the SPA (*Single Page Application*) model.
A SPA is a web application contained in a single HTML document. Components are shown or hidden based on user interaction.

Emphasis is also placed on the correct design of the RESTful API and its implementation in *Express.js*. The server operates using the HTTPS protocol 🔒.

We have used technologies such as *Bootstrap* for element positioning and *MySQL* relational databases managed via *PhpMyAdmin*.

## Summary of the project structure by folder 📁
---------------------------

*   **Helpers:** Reusable methods for view generation, common across the project.
*   **integration:** Data Access Objects (DAOs) for database interactions (retrieving/inserting data).
*   **nbproject:** Internal files used by *NetBeans* IDE.
*   **node_modules:** Modules used by *Node* (server-side).
*   **public:** Publicly accessible files (index page, jQuery, CSS, images, etc.).
*   **routes:** Routers container (mini-web applications with their own routes/middleware). We have `users` and `courses` routers.

The rest of the files contain project metadata (`.json`), the database schema (`.sql`), HTTPS certification files (`.key`, `.crt`), or the application entry point (`app.js`).

## Basic user guide 📖
----------------------

When you enter the planner, you can browse available courses without needing an account. However, to enroll in courses and manage your schedule, registration is required 📝.

When searching for courses, the system checks the database and displays all courses containing the searched string in their title. For example, searching for *cooking* will show all courses with "cooking" in the title.

<p align="center">
<img src="https://github.com/Joncarre/Programacion-web/blob/master/Planificador%20de%20cursos/images/imagen1.png" alt="Searching for courses" style="border-radius: 15px;">
</p>

Clicking on a course shows its details. You must be logged in to register.

<p align="center">
<img src="https://github.com/Joncarre/Programacion-web/blob/master/Planificador%20de%20cursos/images/imagen2.png" alt="Course details view" style="border-radius: 15px;">
</p>

Once registered, you can create courses for others. The system organizes courses, making it easy to see completed courses, current courses, and your weekly schedule 🗓️.

<p align="center">
<img src="https://github.com/Joncarre/Programacion-web/blob/master/Planificador%20de%20cursos/images/imagen3.png" alt="User dashboard/schedule" style="border-radius: 15px;">
</p>
