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


![E-R diagram](https://github.com/afzal9632/BusRservationSystem/assets/101742037/5c53242e-9a78-4cdb-a6d1-c8d2a664596b)


# Swagger UI

![swagger ui](https://github.com/afzal9632/BusRservationSystem/assets/101742037/2419bbcb-b7b6-44ff-ba3e-3400022046a7)


# Admin and Admin Login Controller

![Admin-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/c913f99d-b26c-4819-98a0-eadd8ef28cca)


# User and User Login Controller

![User-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/ea643be8-5c37-4468-bd9f-92c2896d94f7)


# Route Controller

![Route-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/15c0ea2f-3fdb-48ae-99b7-ead14228d9ee)


# Bus Controller


![Bus-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/50a6524f-491e-48a4-99ee-c7778d97c9c6)

# Reservation Controller


![Reservatation-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/b19933f4-3450-49e7-8464-2e2e59a1b6d1)

# Feedback Controller

![Feedback-controller](https://github.com/afzal9632/BusRservationSystem/assets/101742037/7c2a8fdc-7a1f-41fc-af3e-13774bc9db6d)


# Thankyou for visiting this project













