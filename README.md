
# 📁 README Directory

- [🇬🇧 English README](#-english-readme)
- [🇪🇸 Español README](#-readme-en-español)

---

## 🇬🇧 English README

# 🧭 Eureka Server Microservice

This microservice serves as a **Service Registry** in the microservices architecture for the Java Tribe challenge.

### 📌 What is Eureka?

[Eureka](https://github.com/Netflix/eureka) is a component from **Spring Cloud Netflix** that allows microservices to **register and discover each other dynamically** without hardcoding addresses.

### ⚙️ Main Features

- Acts as a **central discovery node**
- Offers a **web UI** at `http://localhost:8761`
- Allows services to:
    - Automatically register themselves
    - Query for other registered services
    - Support failover with instance health checks

### 📦 Main Dependencies

- `spring-cloud-starter-netflix-eureka-server`
- `spring-boot-starter-web`

### 🚀 How to Run Locally

```bash
./mvnw spring-boot:run
```

> Ensure it runs on port `8761`, configured in `application.properties`.

### 🧪 Testing

This microservice contains no business logic and does not require specific unit tests.

### 📂 Project Structure

```
eureka-server
├── src
│   ├── main
│   │   └── java
│   │       └── com.accenture.eureka_server
│   │           └── EurekaServerApplication.java
│   └── resources
│       └── application.properties
└── pom.xml
```

### 🌐 Recommended Configuration

```properties
server.port=8761
eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
eureka.client.service-url.defaultZone=http://localhost:8761/eureka/
spring.application.name=eureka-server
```

### 🧱 Role in the Architecture

This component is part of the **Infrastructure Layer**. It doesn't expose public or private APIs but is essential for **dynamic service registration and discovery** in distributed environments.

---

## 🇪🇸 README en Español

# 🧭 Microservicio Eureka Server

Este microservicio actúa como un **Registro de Servicios (Service Registry)** en la arquitectura de microservicios del desafío técnico de la Tribu Java.

### 📌 ¿Qué es Eureka?

[Eureka](https://github.com/Netflix/eureka) es un componente de **Spring Cloud Netflix** que permite a los microservicios **registrarse y descubrirse dinámicamente** entre sí, sin necesidad de codificar sus direcciones manualmente.

### ⚙️ Funcionalidades Principales

- Funciona como **nodo central de descubrimiento**
- Proporciona una **interfaz web** en: `http://localhost:8761`
- Permite que los servicios:
    - Se registren automáticamente
    - Consulten información sobre otros servicios registrados
    - Implementen tolerancia a fallos mediante chequeos de estado

### 📦 Dependencias Clave

- `spring-cloud-starter-netflix-eureka-server`
- `spring-boot-starter-web`

### 🚀 Cómo Ejecutar Localmente

```bash
./mvnw spring-boot:run
```

> Asegúrate de que esté configurado en el puerto `8761`, mediante `application.properties`.

### 🧪 Tests

Este microservicio no contiene lógica de negocio, por lo que no requiere pruebas unitarias.

### 📂 Estructura del Proyecto

```
eureka-server
├── src
│   ├── main
│   │   └── java
│   │       └── com.accenture.eureka_server
│   │           └── EurekaServerApplication.java
│   └── resources
│       └── application.properties
└── pom.xml
```

### 🌐 Configuración Recomendada

```properties
server.port=8761
eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
eureka.client.service-url.defaultZone=http://localhost:8761/eureka/
spring.application.name=eureka-server
```

### 🧱 Rol en la Arquitectura

Este componente forma parte de la **capa de infraestructura**. No expone APIs, pero es clave para el **registro dinámico y descubrimiento de servicios** en entornos distribuidos.
