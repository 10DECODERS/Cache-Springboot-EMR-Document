# JAVA SPRING BOOT WITH CACHE DATABASE

## What is Intersystem caché database?
  InterSystems Cache is a commercial operational database management system from InterSystems, used to develop software applications for healthcare management, banking and financial services, government, and other sectors. Customer software can use the database with object and SQL code. Caché also allows developers to directly manipulate its underlying data structures: hierarchical arrays known as M technology.
  
## Benefits of Caché database:

  * The object and relational database systems talk directly to the database engine for extremely efficient operation; there is no object-relational middleware or SQL-to-object bridge technology.
  * The logical separation of the database from its physical implementation makes it possible to radically reconfigure application deployments with no change to application logic.
  * Because the database engine interface is open, you can make direct use of its features where needed. This can range from building your own customized database management system to adding targeted optimizations to performance critical applications.

## What is Java spring boot?
  Spring Boot provides a good platform for Java developers to develop a stand-alone and production-grade spring application that you can just run. You can get started with minimum configurations without the need for an entire Spring configuration setup.

## Advantages of Spring boot:
  * Easy to understand and develop spring applications
  * Increases productivity
  * Reduces the development time
  
## What is Maven in spring boot? 
  Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.

## What is Gradle in spring boot?
  Gradle is a build automation system that is fully open source and uses the concepts you see on Apache Maven and Apache Ant. It uses domain-specific language based on the programming language Groovy, differentiating it from Apache Maven, which uses XML for its project configuration. It also determines the order of tasks run by using a directed acyclic graph.

## How can we connect the Spring boot with Cache database?
   *  java spring project using either maven or gradle.
   *  Set the connection of JDBC Driver,Url,Username,Password in gradle’s application properties.
  
![](https://raw.githubusercontent.com/10DECODERS/Cache-Springboot-EMR-Document/assets/1.jpg?raw=true)

  * Adding the JAR files to the local repository for accessing the Cache database.
  * Implement the JAR files in build.gradle.
  * Create a new package and class for dialect.
  
  ![Demo Animation](../assets/2.jpg?raw=true)
  
 ## What are the cache JAR files are needed?
  We need the cache-jdbc-2.0.0.jar to connect the cache database.This jar file can be located in <install-dir>\Dev\java\lib\<java-release>.Then we have to add the JAR file into local repository of  Maven.
	<install-dir> -  Which is the location of cache studio application’s program files in any of system directories like as C:\Program Files\etc.
	<java_release> - Which is the files of Java versions like as JDK17 & JDK18

## How to add the JAR files in Maven local repository?
  Using the following command for adding the external JAR files to Maven repository.
 mvn install:install-file -Dfile=<path-to-file> -DgroupId=<group-id> -DartifactId=<artifact-id> -Dversion=<version> -Dpackaging=<packaging>
	After that we have to implement the JAR files in build.gradle file.
	<path-to-file> - Which is the location of the JAR file like C:\InterSystems\TryCache\dev\java\lib\JDK18\cache-jdbc-2.0.0.jar 
	<group-id> - Which is group name for JAR file depends upon user’s wish.it like as com.intersystems
	<artifact-id> - Name of the JAR file (cache-jdbc)
	<version> - Version of the JAR file(2.0.0)
	<packaging>  - File type (jar)
   
## Output:
  Create the table - We have to start the application at first still the table is created in the cache database.The table name must be the class name.Using the SQL query (SELECT * FROM SQLUser.table_name) to view the table in the Cache database.

 ![Demo Animation](../assets/3.jpg?raw=true)
 ![Demo Animation](../assets/4.jpg?raw=true)
 
## Create Table
 
### Add value: To adding the value to the table using POSTMAN.we have to select the POST method and build the raw data for adding.
 
![Demo Animation](../assets/5.jpg?raw=true)
![Demo Animation](../assets/6.jpg?raw=true)
  
### Update value - To update the value to the table using POSTMAN.we have to select the PUT method and build the raw data for updating.
 
 ![Demo Animation](../assets/7.jpg?raw=true)
 ![Demo Animation](../assets/8.jpg?raw=true)

### Delete value - To delete the value from the table using POSTMAN.we have to select the DELETE method.
  
 ![Demo Animation](../assets/9.jpg?raw=true)
 ![Demo Animation](../assets/10.jpg?raw=true)
  
## What is SWAGGER?
   Swagger allows you to describe the structure of your APIs so that machines can read them. The ability of APIs to describe their own structure is the root of all awesomeness in Swagger. Why is it so great? Well, by reading your API’s structure, we can automatically build beautiful and interactive API documentation. We can also automatically generate client libraries for your API in many languages and explore other possibilities like automated testing. Swagger does this by asking your API to return a YAML or JSON that contains a detailed description of your entire API. 

## How to create the documentation using SWAGGER?
	* Create new class file SwaggerConfig in main application package.
	* Add the connection of swagger in build.gradle.
  
 ![Demo Animation](../assets/11.jpg?raw=true)
 ![Demo Animation](../assets/12.jpg?raw=true)
  
  Then put the url in any browser like this 
    http://localhost:8080/spring-security-rest/api/v2/api-docs
    http://localhost:8080/your-app-root/swagger-ui.html

 ![Demo Animation](../assets/13.jpg?raw=true)




