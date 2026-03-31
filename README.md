# Platform: Eureka Service Registry

### Student Information
- **Student Name**: Dilsara Thiranjaya
- **Student Number**: 2301692050
- **Slack Handle**: Dilsara Thiranjaya
- **GCP Project ID**: dilsara

---


This repository contains the Spring Boot Eureka Service Registry for the Library Management System.

## Architectural Purpose

In a microservices architecture, services need a mechanism to dynamically discover other services instead of relying on hardcoded IP addresses or fully qualified domain names. This application acts as a central **Service Discovery Server**. Microservices register themselves with this server upon startup, and query it to locate other services they need to communicate with.

## Technical Stack

- **Java**: 25
- **Spring Boot**: 4.0.3
- **Spring Cloud**: 2025.1.0
- **Build Tool**: Maven

### Configuration Integration

It is configured to fetch its environment properties at runtime from the centralized Config Server component. The application will look for the Config Server at `http://config.platform:9000`.

## Running the Application

Ensure the Config Server is up and accessible before starting the Service Registry.

```bash
mvn spring-boot:run
```