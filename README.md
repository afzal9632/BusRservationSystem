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
https://localhost:8888/
```
```
http://localhost:8888/swagger-ui/
```
# API Module Endpoints
## Login Module
POST //login/admin : Admin can login with mobile number and password provided at the time of registation
## Sample API Response for Admin Login
POST   localhost:8888/login/admin

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
