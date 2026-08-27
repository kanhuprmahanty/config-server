# 🚀 Spring Cloud Config Server

> **Centralized Configuration Management for Spring Boot Microservices**

A production-style **Spring Cloud Config Server** that provides centralized, externalized, and environment-specific configuration for distributed Spring Boot microservices. Configuration is maintained in a Git repository and dynamically served to client services through REST endpoints.

---

## 📌 Overview

In a microservices architecture, maintaining configuration separately inside every service can become difficult and error-prone.

This project solves that problem by providing a **centralized configuration server**.

```text
                         ┌──────────────────────┐
                         │    Git Repository    │
                         │                      │
                         │ application.yml      │
                         │ user-service.yml     │
                         │ order-service.yml    │
                         │ product-service.yml  │
                         └──────────┬───────────┘
                                    │
                                    │ Configuration
                                    ▼
                         ┌──────────────────────┐
                         │   Config Server      │
                         │                      │
                         │ Spring Boot          │
                         │ Spring Cloud Config  │
                         │ Port: 8888           │
                         └──────────┬───────────┘
                                    │
                    ┌───────────────┼───────────────┐
                    │               │               │
                    ▼               ▼               ▼
             ┌────────────┐  ┌────────────┐  ┌────────────┐
             │   User     │  │   Order    │  │  Product   │
             │  Service   │  │  Service   │  │  Service   │
             └────────────┘  └────────────┘  └────────────┘
