# 🎵 RevPlay - Microservices Architecture

RevPlay is a full-stack cloud-native music streaming platform, evolved from a monolithic application into a scalable microservices-based system.

This repository acts as a **parent orchestration layer**, integrating multiple independent microservices using **Git submodules**, enabling modular development and centralized deployment.

---

## 🧠 Project Evolution

* **P1** → Console-based Java Application
* **P2** → Monolithic Web Application (Spring Boot + Angular + MySQL)
* **P3** → Cloud-Native Microservices Architecture

> “RevPlay evolved from a monolithic system into a cloud-native microservices architecture to improve scalability, maintainability, and deployment flexibility.”

---

## 🏗️ Architecture Overview

The system is divided into multiple independent services:

### 🔹 Core Services

* **User Service** → Authentication, user/artist profiles, role management
* **Catalog Service** → Songs, albums, artists management
* **Playlist Service** → Playlist creation and management
* **Playback Service** → Music playback and tracking
* **Favorites Service** → User liked songs
* **Analytics Service** → Play counts, user insights, engagement metrics

### 🔹 Infrastructure Services

* **API Gateway** → Central entry point for routing requests
* **Eureka Server** → Service discovery and registration
* **Config Server** → Centralized configuration management

### 🔹 Shared Module

* **Security Module** → JWT authentication and role-based authorization

### 🔹 Frontend

* **Angular Application** → UI for listeners and artists

---

## 📁 Repository Structure (Git Submodules)

```bash
revplay-microservices/
│
├── revplay-user-service
├── revplay-catalog-service
├── revplay-playlist-service
├── revplay-playback-service
├── revplay-favorites-service
├── revplay-analytics-service
├── revplay-api-gateway
├── revplay-config-server
├── revplay-eureka-server
├── revplay-frontend
├── revplay-security
└── .gitmodules
```

Each service is maintained as an **independent repository** and integrated via **Git submodules**.

---

## ⚙️ Technologies Used

### Backend

* Java 21
* Spring Boot
* Spring Security (JWT)
* Spring Cloud (Eureka, Config Server, Gateway)
* OpenFeign (Inter-service communication)

### Frontend

* Angular

### Database

* MySQL / Oracle 10g

### DevOps (Planned)

* Docker
* Kubernetes

---

## 🚀 Getting Started

### 🔹 Clone Project (IMPORTANT)

```bash
git clone --recurse-submodules https://github.com/dharam8218/revplay-microservices.git
```

---

## ▶️ Running the Application

Follow this order to start the system:

1. Start **Config Server** (port 8888)
2. Start **Eureka Server** (port 8761)
3. Start all backend microservices
4. Start **API Gateway**
5. Start **Angular Frontend (port 4200)**

---

## 🔄 Development Workflow

### 🔹 Update any microservice

```bash
cd revplay-user-service
git add .
git commit -m "feature/update"
git push
```

### 🔹 Update main repository reference

```bash
cd ..
git add revplay-user-service
git commit -m "updated submodule reference"
git push
```

---

## 🔐 Security Implementation

* JWT-based authentication
* Role-based authorization (**USER / ARTIST / ADMIN**)
* Centralized security module shared across services
* Secure API Gateway routing

---

## 📊 Key Features

* User and Artist registration/login
* Song upload and management
* Playlist creation and management
* Favorites system
* Music playback with tracking
* Real-time analytics (plays, engagement)
* Role-based access control
* Microservices communication via Feign Clients

---

## ⚡ Challenges Solved

* Designed and migrated architecture from monolith → microservices
* Implemented inter-service communication using OpenFeign
* Managed centralized authentication with JWT
* Resolved CORS issues using API Gateway
* Maintained independent service databases
* Handled distributed system debugging and logging

---

## 💡 Why Microservices?

* Independent deployment of services
* Better scalability and flexibility
* Fault isolation between services
* Improved maintainability
* Real-world cloud-native architecture

---

## 👨‍💻 Author

**Dharamveer Singh**
📍 India
📧 [dharamveersinghgtb@gmail.com](mailto:dharamveersinghgtb@gmail.com)
🔗 https://github.com/dharam8218

---

## ⭐ Future Enhancements

* Docker containerization for all services
* Kubernetes deployment (cluster-based scaling)
* CI/CD pipeline (GitHub Actions)
* API rate limiting & monitoring
* Distributed tracing (Zipkin / Sleuth)
* Centralized logging system

---
