# Group 19 CS2810 Team Project - Oaxaca Restaurant System
## About

This system is a project created by Group 19 2021. It implements a complete restaurant system webapp with a working MSSQL database with JDBC integration, Java backend, Spark for API call management and HTML, Javascript and CSS frontend. Stripe is our payment partner, used for handling payments from customers.

## Setup
### Requirements
* Eclipse IDE (JRE 1.8)
* Maven
* Browser
* JDBC
* Stripe
* Database Management Software (Optional)
* API Client (Optional)

### Maven Dependencies
* **JUnit Jupiter** - Used for writing unit tests
* **Spark Java** - Used as the foundation for our web server
* **SLF4J** - Used for log messages by Spark
* **Gson** - Used to handle JSON within Java
* **MSSQL-JDBC** - Used to interact with the MSSQL database
* **JWT** - Used to create and verify JWT tokens (used for authentication)
* **Lombok** - helps generate getters, setters and other useful methods
* **Stripe** - Used for making a payment to the restaurant for an order
* **Maven Surefire** - Used for the generation of javadoc and a runnable jar file of the project

### Installation
To setup the server so that it can run locally, you must:
* Clone the project repo
* Add database connection information in database.properties
* Add your own secret key to authentication.properties
* Change the port that the server runs on (optional, default 5000)
* Run Server.java
* Navigate to localhost:(port)/

### Testing
Click [here](http://oaxaca.visagie.co.uk/) for live website.  
To access the login screen, click [here](http://oaxaca.visagie.co.uk/login.html).  
The username is admin and the password is supersecretpassword! to access all views.  

You can also test the server yourself by downloading this [fully working jar file](https://github.com/RHUL-CS-Projects/TeamProject2021_19/tree/master/runnable%20Jar)

### Stripe Integration
Maven users will need to add this dependency to the project's POM if it is not already there:

```xml
<dependency>
  <groupId>com.stripe</groupId>
  <artifactId>stripe-java</artifactId>
  <version>20.42.0</version>
</dependency>
```
To setup the project for customers to pay into your own stripe account you will need to change the stripe API key.
Your secret key can be found on your stripe dashboard in API keys under Developers.
You can then copy and paste this key into OrderAPI on line 402.

## Documentation
* [Web API Documentation](http://oaxaca-docs.visagie.co.uk/WebAPIDocumentation/)
* [Data access objects (DAO) Documentation](https://github.com/RHUL-CS-Projects/TeamProject2021_19/blob/master/design%20docs/Backend%20Design%20Specification.pdf)
* [Database Structure](https://github.com/RHUL-CS-Projects/TeamProject2021_19/blob/master/design%20docs/restaurant_schema_final.PNG)
* [Javadoc](http://oaxaca-docs.visagie.co.uk/BackendDocumentation/)
* [JSdoc](http://oaxaca-docs.visagie.co.uk/FrontendDocumentation/)
* [Video Demonstration](https://www.youtube.com/watch?v=GS0yyh4_uW0)
