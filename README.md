# Job Portal – Spring Boot Microservices

A microservices-based Job Portal backend application built using Spring Boot.  
The system is divided into independent services for Job, Company, and Review management, following the database-per-service pattern with centralized configuration using Spring Cloud Config Server.

---

## 🚀 Architecture Overview

This project follows a distributed microservices architecture:

- Job Service – Manages job postings
- Company Service – Manages company details
- Review Service – Manages job/company reviews
- Eureka Server – Service discovery
- Config Server – Centralized configuration management

Each service runs independently and communicates via REST APIs.

---

## 🏗️ Microservices

### 1️⃣ Job Service
- Create, update, delete job postings
- Fetch job details along with company information
- Fetch reviews related to a job
- Communicates with Company & Review services

### 2️⃣ Company Service
- Manage company information
- One-to-many relationship with jobs

### 3️⃣ Review Service
- Add and fetch reviews for jobs
- Maintains rating and feedback details

---

## ⚙️ Infrastructure Services

### 🔎 Eureka Server
- Service registration and discovery
- Enables dynamic service lookup

### 🗂️ Config Server
- Centralized configuration management
- Externalized properties for all services
- Supports environment-based configuration

---

## 🔧 Tech Stack

- Java 17
- Spring Boot
- Spring Data JPA
- Spring Web
- MySQL / H2
- Spring Cloud Eureka
- Spring Cloud Config
- OpenFeign (for inter-service communication)
- Maven

---

## 📌 Architecture Pattern

- Microservices Architecture
- Database per Service
- Centralized Configuration Pattern
- RESTful Communication
- Service Discovery (Eureka)

---

## 🔄 Service Communication Flow

Job Service → Fetch Company details via Company Service  
Job Service → Fetch Reviews via Review Service  

All services:
- Register with Eureka Server
- Fetch configuration from Config Server at startup

---


