# Taxi Service
***
A small web application for working with various taxi services.
* To use this program you need to **register** and **log in**.
* You can see a list of all registered `drivers`.
* It is possible to get a list of all `cars` entered into the database, as well as the `manufacturers` of these cars.
* An authenticated user can see a table with all his cars.
* There are pages for **adding** new drivers, cars and manufacturers.
* There is a function of adding a driver to the car.
* The application is deployed on **Heroku** server, so you can access it by following this [link](https://damp-fortress-14433.herokuapp.com).
## Configuration
***
* This project has 3 models for `driver`, `manufacturer` and `car` respectively.
* On top of the project structure dao tier is located with the corresponding interfaces and their implementations which have functions that sends queries to database.
* **Services** with which the user will work directly are located under the **DAO layer**.
* In order to comply with the principle of **dependency injection**, the `Injector class` with annotations has been created.
* Each page of this web application has its own `Servlet Controller` and `.jsp` files to handle different types of requests from users.
## Technology
* **SOLID and Dependency injection** principles are followed in this project.
* **Java Database Connectivity** is used to connect to the database and process requests.
* Each DAO class has **CRUD** operations.
* **Servlet controllers** are used here to handle HTTP requests.
## How to use
***
The project can be run either locally or in the cloud
### Run locally
1. To build an application it is required to run: `mvn package` in terminal.
2. And then run an app using the java command: `java -jar target/dependency/webapp-runner.jar target/*.war`.
3. The program will start up on port **8080**, you can open it at the link *http://localhost:8080/*.
### Run in the cloud
1. Likewise, it is needed to run: `mvn package`.
2. Create the app by running: `heroku create`.
3. Deploy the code to heroku server: `git push heroku main`.
4. To open app in browser: `heroku open`.
