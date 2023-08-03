# REST API for Bus Reservation System Portal
- This REST API for a Bus Reservation System Portal Application performs all the fundamental CRUD operations of any Bus Reservation Application platform with user validation at every step.
# Tech Stack
- Java
- Spring Framework
- Spring Boot
- Spring Data JPA
- Hibernate
- MySQL
# Modules
- Login, Logout Module
- Admin Module
- User Module
- Route Module
- Bus Module
- Reservation Module
- Feedback Module
# Features
- User and Admin authentication & validation with session uuid.
- Admin Features:
  - Administrator Role of the entire application
  - Only registered admins with valid session token can add/update/delete route and bus from main database
  - Admin can access the details of different users and reservations.
- User Features:
  - Registering themselves with application, and logging in to get the valid session token
  - Viewing list of available buses and booking a reservation
  - Only logged in user can access his reservations, profile updation and other features.
 
# Installation & Run
Before running the API server, you should update the database config inside the [application.properties](https://github.com/afzal9632/BusRservationSystem/blob/main/src/main/resources/application.properties) file.
Update the port number, username and password as per your local database config.

```
    server.port=8880

    spring.datasource.url=jdbc:mysql://localhost:3306/busdb
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    spring.datasource.username=root
    spring.datasource.password=root
```
# API Root Endpoint
```
https://localhost:8880/
```
```
http://localhost:8880/swagger-ui/
```
# API Module Endpoints
## Login Module
POST //login/admin : Admin can login with mobile number and password provided at the time of registation
## Sample API Response for Admin Login
POST   localhost:8880/login/admin

- Request Body
```
{
  "adminPassword": "Logintoadmin7643",
  "mobileNumber": "7903661933"
}
```
- Response
```
Response body
{
  "adminId": 4,
  "uuid": "IJYhDn",
  "dateTime": "2023-08-02T18:05:52.4142812"
}
```
# E-R Diagram Of Bus Application


![E-R diagram](https://github.com/afzal9632/BusRservationSystem/assets/101742037/9fddd41e-6bc8-4d43-a4f4-f7b19a6b9c8b)

# Swagger UI

![swagger ui](https://github.com/afzal9632/BusRservationSystem/assets/101742037/660b14f1-c0d2-4dfd-bfea-5fb206ec6cbf)

# Admin and Admin Login Controller

![Admin-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/568fee49-772e-41c1-a7f9-57df1953c3ec)

# User and User Login Controller

![User-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/c7166232-810f-428e-84a0-1e6fad244786)

# Route Controller

![Route-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/2c6a751b-79be-4489-a506-10e7ffeb5a76)

# Bus Controller

![Bus-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/8a2965bc-c3ec-410f-88c0-3b434d4774fa)

# Reservation Controller

![Reservatation-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/62469e9c-d263-4cc2-b343-8d80938b74ca)

# Feedback Controller

![Feedback-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/3871a6a0-1237-4450-ae6c-12c328af0a77)


# Thankyou for visiting our project












