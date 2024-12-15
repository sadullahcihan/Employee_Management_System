Employee Management System
Employee Management System (EMS) is a simple application that manages employee data. This application allows you to add, update, delete, and list employees. Users can save employee information and manage employees within the system.

Technologies
Spring Boot: Backend framework for the application.
JPA (Java Persistence API): ORM framework used for database operations.
H2 Database (or PostgreSQL/MYSQL can be used): The database used for storing data.
Spring Security: For security and authentication purposes.
IntelliJ IDEA: Development environment.

Features
Add, update, and delete employees.
List employees.
Validate and manage employee information.
Perform operations through RESTful APIs.
Overview of the Application
This project is a simple application for managing employees. Users can manage employee data through REST APIs.

Application Flow
Add Employee: Adds a new employee record.
List Employees: Lists all employees.
Update Employee: Updates an existing employee record.
Delete Employee: Deletes an existing employee record.

Getting Started
Prerequisites
JDK 17 or higher.
Spring Boot 3.x or higher.
Git (to clone the project).
Maven or Gradle (for dependency management).

Project Setup
1- Clone this project from GitHub:
git clone https://github.com/your-username/employee-management-system.git
cd employee-management-system

2-To build the Spring Boot project, use Maven or Gradle:

Using Maven:
./mvnw spring-boot:run

3-The application will run by default at http://localhost:9090. You can open this URL in your browser to access the application.

Database Configuration
The project uses the H2 database by default, but you can configure PostgreSQL/MySQL if needed. To use PostgreSQL, modify the src/main/resources/application.properties file as follows:
spring.datasource.url=jdbc:postgresql://localhost:5432/ems
spring.datasource.username=postgres
spring.datasource.password=your-password
spring.jpa.hibernate.ddl-auto=update

If using H2, you can skip this step as H2 is configured by default.

***
API Usage
1. Add Employee
URL: /api/employees

Method: POST

Body (JSON):
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@example.com"
}

Response (JSON):

{
  "id": 1,
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@example.com"
}

2. List Employees
URL: /api/employees

Method: GET

Response (JSON):
[
  {
    "id": 1,
    "firstName": "John",
    "lastName": "Doe",
    "email": "john.doe@example.com"
  },
  {
    "id": 2,
    "firstName": "Jane",
    "lastName": "Smith",
    "email": "jane.smith@example.com"
  }
]

3. Update Employee
URL: /api/employees/{id}

Method: PUT

Body (JSON):
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@newdomain.com"
}

Response (JSON):
{
  "id": 1,
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@newdomain.com"
}

4. Delete Employee

URL: /api/employees/{id}
Method: DELETE
Response: 
"Employee with id: 2 deleted successfully."
