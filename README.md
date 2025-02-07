# GymCRM – Comprehensive Gym Management System  

GymCRM is a **Spring Boot-based CRM solution** tailored for gyms, featuring **secure user management**, **trainer and trainee operations**, and **training scheduling**. It follows a **microservices architecture** and integrates **Spring Security**, **ActiveMQ messaging**, and **Swagger UI** for API interaction.  

## 🏗️ Architecture  

🔹 **Discovery Server** – Service registry for dynamic service discovery.  
🔹 **Main Module** – Core CRM functionalities with **MySQL** for data persistence.  
🔹 **Reporting Microservice** – Handles reporitng for trainers using **MongoDB**, communicates via **ActiveMQ**.  

## 🚀 Features  

- **User Management** – Secure authentication and access control.  
- **Trainer & Trainee Operations** – Profile management, activation/deactivation.  
- **Training Management** – Create, assign, and track gym sessions.  
- **Microservices Communication** – Uses **ActiveMQ** for seamless integration.  
- **API Documentation** – Interactive API via **Swagger UI**.  
- **Secure Access** – **Spring Security** ensures protected endpoints.  
- **Docker Support** – Easily deployable with **Docker Compose**.  

## 🛠️ Getting Started  

### **1️⃣ Run the Discovery Server**  
```bash
cd discovery-server
mvn spring-boot:run
```

### **2️⃣ Run the Main Module**  
```bash
cd gym-crm-module
mvn spring-boot:run
```

### **3️⃣ Start the Microservice**  
```bash
cd trainer-microservice
mvn spring-boot:run
```

## 🔗 API Documentation  

Once the **Main Module** is running, access the **Swagger UI** at:  

🔗 [localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

## 🐳 Docker Deployment  

To deploy the entire application using **Docker Compose**, follow these steps:  

### **1️⃣ Build the Application**  
Ensure all services are built before running the containers:  
```bash
mvn clean package -DskipTests
```

### **2️⃣ Run Docker Compose**  
Navigate to the root directory containing the **docker-compose.yml** file and start the services:
```bash
docker-compose up -d
```

### **3️⃣ Verify Running Containers**  
Check if all services are running properly:
```bash
docker ps
```


