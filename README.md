# 🚕TAXI SERVICE🚕
A basic taxi service project that allows a driver acting as a user to manage data records located in a remote database.
## ✨Features✨
* Register a new user by creating a driver
* Login as a driver
* Logout
* Display all cars/manufacturers/drivers/driver cars
* Create new car/manufacturer
* Add driver to car
## 🚀Try it yourself on Heroku!🚀
By going to: https://taxi-service989.herokuapp.com

DB host: https://console.clever-cloud.com
###### Upd: Starting November 28th, 2022, free dynos will no longer be available.

## 🧬Project structure🧬
### N-tier architecture
**Project built by using N-tier architecture divides application
into logical layers:** 
* **Presentation tier**: UI is represented by a JSP, translated into a Java servlet/Controller and executed on the server.
* **Logic tier**: business logic service classes that move and process data between the data and presentation layers.
* **Data tier**: data store/retrieve layer.
### DB structure
![img.png](img.png)

## 👩‍💻Technologies👩‍💻
* Apache Maven
* JDK 11 
* JDBC
* MySQL 8
* Tomcat 9
* JSTL
* JSP
* Servlet API

## 🛠Setup guide🛠

#### To run this project locally on your computer, first of all, you need to make sure you have the following components installed:
* JDK 11 ([installation guide](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html))
* IntelliJ IDEA Ultimate ([download here](https://www.jetbrains.com/idea/download/#section=windows))
* Apache Maven ([download here](https://maven.apache.org/download.cgi), [installation guide](https://maven.apache.org/install.html))
* MySql ([installation guide](https://dev.mysql.com/doc/mysql-installation-excerpt/8.0/en/))
* Tomcat 9 ([installation guide](https://medium.com/@ngotantien/how-to-install-apache-tomcat-9-on-windows-mac-os-x-ubuntu-and-get-started-with-java-servlet-45f959d7ee0a))

### Application configuration
#### Create a new MySQL connection
Using [MySql Workbench](https://dev.mysql.com/downloads/workbench/) create a new connection by following this [guide](https://dev.mysql.com/doc/workbench/en/wb-getting-started-tutorial-create-connection.html).

#### Create a new DB
Clone this repository. To create a new DB with required tables to work with in project directory open [`src/main/resources`](src/main/resources) folder. Find file [`init_db.sql`](src/main/resources/init_db.sql) and copy SQL script from it. Move the copied script to editor panel, then execute it.

#### Connect DB to project
To connect the created database to the project follow this [guide](https://www.jetbrains.com/help/idea/mysql.html).
Fill in the fields with the values that you specified when creating the connection in MySql Workbench.
Also you need to edit fields in file [`ConnectionUtil.java`](src/main/java/taxi/util/ConnectionUtil.java) according to previously entered values.
```
   private static final String URL = "URL";
   private static final String USERNAME = "USER NAME";
   private static final String PASSWORD = "PASSWORD";
   private static final String JDBC_DRIVER = "JDBC DRIVER";
```

#### Tomcat server setup
For TomCat server setup follow [this](https://mkyong.com/intellij/intellij-idea-run-debug-web-application-on-tomcat/) configuration guide.
