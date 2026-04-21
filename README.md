# java-microservice-cicd-pipeline
# Java Spring Boot Microservice: AWS ECS Deployment

This project demonstrates a production-ready CI/CD workflow for a Java microservice. It is designed to be built with **AWS CodeBuild** and deployed to **Amazon ECS (Fargate)** via **AWS CodePipeline**.

## 🚀 Key Features
*   **Java 17 & Spring Boot**: Modern backend architecture.
*   **Dockerized**: Includes a multi-stage Dockerfile for optimized container images.
*   **CI/CD Ready**: Pre-configured `buildspec.yml` for automated AWS builds.
*   **High Availability**: Includes automated Health Checks for AWS Task Definitions.

## 🛠 Tech Stack
*   **Language:** Java 17
*   **Framework:** Spring Boot 3.x
*   **Containerization:** Docker
*   **CI/CD:** AWS CodePipeline, CodeBuild, ECR (Elastic Container Registry)
*   **Orchestration:** Amazon ECS (Fargate)

## 📋 Prerequisites
*   AWS Account with CLI access.
*   Docker installed and running.
*   Java 17+ and Maven.

## ⚙️ Deployment Configuration
### AWS Task Definition Health Check
To ensure zero-downtime deployment, use the following command in your ECS Task Definition:
```bash
CMD-SHELL, curl -f http://localhost:8080/actuator/health || exit 1
