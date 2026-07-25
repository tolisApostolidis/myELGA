# Table of Contents
* [About](#about)
* [Requirements](#requirements)
* [Database Setup](#database-setup)
* [Configuration](#configuration)
* [How to Run Backend (Server)](#how-to-run-backend-server)
* [How to Run Frontend](#how-to-run-frontend)
* [Application Ports](#application-ports)
* [Features](#features)




# About
myELGA is a full-stack application designed to simulate a real-world citizen service management platform for compensation related to farming and livestock activities.

Built with **Spring Boot** and **Vue 3**, the system demonstrates:

- **REST API** design
- **Role-based** authentication
- **Frontend–Backend** integration

The project reflects modern software engineering practices with an emphasis on scalability, maintainability, and automation.

# Requirements
In order to execute this application (hereafter referred to as "the app") successfully, you must install the following tools:
* [ ] Install Java JDK
  * 21 = recommended version (same as the build version)
* [ ] Install Maven
  * 3.9+
  * 3.9.9. = recommended version (same as the build version)
* [ ] Install Node
  *  18+ (required for Vite)
  *  22.15.1. = recommended version (same as the build version)

---

# Database Setup

Before running the backend server, create the required MySQL database:

```sql
CREATE DATABASE elga_app_schema;
```

---

# Configuration

Before running the backend server, you must configure the application properties.

1. Navigate to application properties file
```java
$ cd backend/src/main/resources/
```
2. Find applications.properties and open it
3. Fill in your database, e-mail and JWT credentials
4. Rename file to "application.properties"


---


# Initialize Data Setup

The project includes a class named `InitializeDatabase`. This class contains a `@PostConstruct` method that automatically creates
three default users one for each role.

By default, the initialization logic is commented out to prevent
duplicate data creation.

If you want to generate the default users:

1. Open the `InitializeDatabase` class (follow backend/src/java/com/hua/myElga/config/)
2. Uncomment lines 27–31.
3. Start the application once.
4. After the users are created, comment the lines again.

⚠️ This step should be performed only **once**.


---
   
    
# How to run Backend (Server)
To run the app's backend (server), run below commands:
```java  
$ cd backend

$ mvn clean package

$ java -jar target\myElga-0.0.1-SNAPSHOT.jar
```

---


# How to run frontend
To run the app's frontend, run below commands:
```java  
$ cd frontend

$ npm install

$ npm run
```

---


# Application Ports
The application runs on the following ports during local development:
<table>
  <thead>
     <tr>
       <th>Component</th>
       <th>Port</th>
       <th>URL</th>
     </tr>
 </thead>
 <tbody>
    <tr>
       <td>Backend (Spring Boot)</td>
       <td>8080</td>
       <td>http://localhost:8080</td>
    </tr>
    <tr>
       <td>Frontend (Vue + Vite</td>
       <td>5173</td>
       <td>http://localhost:5173</td>
    </tr>
  </tbody>
</table>


---


# Features
Below are the features that are provided by the app
<table>
  <thead>
     <tr>
       <th>Feature</th>
       <th>✅</th>
       <th>❌</th>
       <th>⌛</th>
     </tr>
 </thead>
 <tbody>
    <tr>
       <td>User authentication (JWT)</td>
       <td>✔</td>
       <td></td>
       <td></td>
    </tr>
    <tr>
        <td>Role-based access controls</td>
        <td>✔</td>
        <td></td>
        <td></td>
     </tr>
    <tr>
        <td>Email notifications</td>
        <td>✔</td>
        <td></td>
        <td></td>
     </tr>
     <tr>
         <td>SMS notifications</td>
         <td></td>
         <td>✔</td>
         <td></td>
     </tr>
    <tr>
         <td>Docker support</td>
         <td></td>
         <td></td>
         <td>✔</td>
     </tr>
    <tr>
         <td>Jenkins CI/CD</td>
         <td></td>
         <td></td>
         <td>✔</td>
     </tr>
    <tr>
         <td>Kubernetes deployement</td>
         <td></td>
         <td></td>
         <td>✔</td>
     </tr>
    <tr>
         <td>Ansible automation</td>
         <td></td>
         <td></td>
         <td>✔</td>
     </tr>
  </tbody>
</table>


---


![Java](https://img.shields.io/badge/Java-21-orange?logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.1.5-6DB33F?logo=springboot&logoColor=white)![JWT](https://img.shields.io/badge/JWT-Authentication-black?logo=jsonwebtokens&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue.js-3-4FC08D?logo=vue.js&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
