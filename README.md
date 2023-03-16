# Mike Vlasoff, Delta

Spring MVC CRUD project. It has 2 quests out of the box.
1. Create MySQL database from db_dump.sql file in resources.
2. Use Tomcat 9.
3. Artifact: quest-delta:war exploded
4. Application context: /
5. Start URL: http://localhost:8080/
6. Project is ready to be deployed in Docker containers. jdbc:p6spy:mysql://localhost:3306/todo (AppConfig).
   /root/style/main.css, /root/script/jquery.js, /root/script/my.js (tasks.html)

Tools used: Java 17, Intellij IDEA U, MySQL, Spring MVC, Hibernate, Thymeleaf, Docker.


Requirements:

You need to make a list of tasks (todo-list) with the ability to view the list of tasks, add new tasks, edit and delete existing tasks.
It is advisable not to use Spring Boot, but to figure out how to configure everything yourself.
1. Deploy sql script.
2. Create a new Maven project.
3. Add the dependencies you need to work with MySQL, Hibernate, Spring, Spring MVC, Thymeleaf.
4. Add an entity layer to the project ('domain' package). Add a 'Task' class - it will be responsible for the task in the to-do list. 
Required fields: 'description' – task description, 'status' – task execution status. Use Enum as the status.
5. Add package 'config'. In it, place the necessary classes for setting up a Spring MVC application, working with a database (via Hibernate), and all other settings.
6. Add a 'dao' layer, which should contain the 'TaskDAO' class, which will be responsible for working with the database. Methods that should be - CRUD and paging support.
7. Add a service layer where you place the logic for creating and editing tasks.
8. Now the controller layer. It should have methods:
 - get a list of tasks (including paging), 
 - add a new task, 
 - edit an existing task, 
 - submit a task.
Think over what methods and their mappings should be.
9. The last step is the template (html or js file). Optionally, you can move styles and scripts to different files by type. 
As usual, for a backend developer, functionality is important, not appearance, so what the visual of the application will be is up to you.

Optional task:
Package the application in a docker container, add a docker-compose file where configure the application-database bundle in docker containers.

