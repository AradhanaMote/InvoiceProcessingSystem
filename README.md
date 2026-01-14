# Invoice Processing System

A simple Invoice Processing System built with React (Material UI) for the frontend and Spring Boot + Hibernate for the backend, using MySQL as the database.

## Tech stack
- Frontend: React, Material UI
- Backend: Spring Boot, Hibernate (JPA)
- Database: MySQL
- Build tools: npm/yarn (frontend), Maven (backend)

## Features (basic)
- Create, view, update, and delete invoices
- List and search invoices
- Basic form validation and UI using Material UI
- Backend REST API with persistent storage (MySQL)

## Prerequisites
- JDK 11+ (or version required by the project)
- Maven (or use the provided Maven wrapper `./mvnw`)
- Node.js + npm or yarn
- MySQL server

## Database setup
1. Create a database in MySQL:
   - Example:
     CREATE DATABASE invoice_db;
2. Create a user or use an existing one and grant privileges:
   - Example:
     CREATE USER 'invoice_user'@'localhost' IDENTIFIED BY 'your_password';
     GRANT ALL PRIVILEGES ON invoice_db.* TO 'invoice_user'@'localhost';
3. Update backend configuration (`application.properties` or `application.yml`) with your DB settings:
   - Example `application.properties`:
     spring.datasource.url=jdbc:mysql://localhost:3306/invoice_db?useSSL=false&serverTimezone=UTC
     spring.datasource.username=invoice_user
     spring.datasource.password=your_password
     spring.jpa.hibernate.ddl-auto=update

## Quick start

### Backend (Spring Boot)
1. Navigate to the backend folder (if applicable):
   cd backend
2. Build and run:
   - With Maven:
     ./mvnw spring-boot:run
     or
     mvn spring-boot:run
   - Or build a jar and run:
     mvn package
     java -jar target/your-backend-artifact.jar

The backend will expose REST endpoints (commonly on http://localhost:8080).

### Frontend (React + Material UI)
1. Navigate to the frontend folder (if applicable):
   cd frontend
2. Install dependencies:
   npm install
   or
   yarn
3. Start the development server:
   npm start
   or
   yarn start

The frontend typically runs on http://localhost:3000 and should be configured to call the backend API (CORS settings may be required).

## Build for production
- Frontend:
  npm run build
  or
  yarn build
- Backend:
  mvn package

## Environment notes
- Adjust API base URLs in the frontend environment/config files to point to the backend.
- Ensure CORS is enabled in the backend for the frontend origin during development.

## Contributing
Feel free to open issues or submit pull requests for improvements or bug fixes.
