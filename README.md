# SpringCloudConfigServerEx

A simple Spring Cloud microservice that registers itself with **Eureka Server** for service discovery.  
This project is part of my learning journey in **Microservices with Spring Boot & Spring Cloud (PW Skills)**.

---

## 🧩 Project Overview

- Registers the application as a **Eureka Client**.
- Uses **Eureka Service Discovery** so other microservices can find and communicate with this service.
- Demonstrates how to configure `application.properties` for a Spring Cloud–based microservice.

---

## 🔧 Tech Stack

- **Language**: Java  
- **Framework**: Spring Boot, Spring Cloud  
- **Service Discovery**: Netflix Eureka  
- **Build Tool**: Maven  
- **Config File**: `application.properties`

> Keywords (ATS-friendly): *Java, Spring Boot, Spring Cloud, Microservices, Eureka Client, Service Discovery, Maven, REST, Cloud Native Applications*

---

## ⚙️ Configuration (application.properties)

This is the core configuration used in this project:

```properties
my.app.title=PW SKILLS

# setting up instance id
eureka.instance.instance-id=${spring.application.name}:${random.value}

# register with eureka
eureka.client.register-with-eureka=true

# enable other MS to interact
eureka.client.fetch-registry=true

# setting up URL of Eureka server
eureka.client.service-url.defaultZone = http://localhost:8761/eureka
