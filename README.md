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
  
![](https://raw.githubusercontent.com/10DECODERS/Cache-Springboot-EMR-Document/master/1.jpg)

  * Adding the JAR files to the local repository for accessing the Cache database.
  * Implement the JAR files in build.gradle.
  * Create a new package and class for dialect.
  
  ![](https://raw.githubusercontent.com/10DECODERS/Cache-Springboot-EMR-Document/master/2.jpg)
  
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

 ![](https://raw.githubusercontent.com/10DECODERS/Cache-Springboot-EMR-Document/master/3.jpg)
 
 ![](https://raw.githubusercontent.com/10DECODERS/Cache-Springboot-EMR-Document/master/4.jpg)
 
 ### Create Table
 
  ![](https://raw.githubusercontent.com/10DECODERS/Cache-Springboot-EMR-Document/master/5.jpg)
  
  ![](https://raw.githubusercontent.com/10DECODERS/Cache-Springboot-EMR-Document/master/6.jpg)
  
  ### Add value




