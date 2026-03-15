# Kubernetes Web App Deployment

## Overview
This project demonstrates a complete DevOps pipeline for building, containerizing, and deploying a Java web application using modern DevOps tools.

The project automates the process of:
- Building a Java application using Maven
- Containerizing the application using Docker
- Automating infrastructure setup using Ansible
- Creating a CI/CD pipeline using Jenkins
- Deploying the application to Kubernetes

This repository showcases practical DevOps skills such as CI/CD automation, containerization, infrastructure automation, and Kubernetes orchestration.

---

## Architecture

Developer  
↓  
GitHub Repository  
↓  
Jenkins CI/CD Pipeline  
↓  
Maven Build  
↓  
Docker Image Build  
↓  
Push Image to Registry  
↓  
Kubernetes Deployment  
↓  
Application running on Kubernetes Cluster

---

## Tech Stack

| Category | Tools Used |
|--------|-------------|
| Programming Language | Java |
| Build Tool | Maven |
| Containerization | Docker |
| Container Orchestration | Kubernetes |
| Configuration Management | Ansible |
| CI/CD | Jenkins |
| Version Control | Git / GitHub |

---

## Project Structure

```
kubernetes_webapp_deploy
│
├── ansible/
│   └── playbooks for infrastructure automation
│
├── Docker-files/
│   └── Dockerfile for building the application container
│
├── kubedefs/
│   └── Kubernetes manifests (deployment, service, ingress)
│
├── src/
│   └── Java web application source code
│
├── Jenkinsfile
│   └── Jenkins CI/CD pipeline definition
│
├── docker-compose.yml
│   └── Used for running multi-container setup locally
│
├── pom.xml
│   └── Maven project configuration
│
└── README.md
```

---

## CI/CD Pipeline Workflow

The Jenkins pipeline performs the following stages:

1. Pull Source Code  
   Jenkins fetches the code from GitHub.

2. Build Application  
   Maven compiles and packages the Java application.

3. Build Docker Image  
   Docker builds a container image for the application.

4. Push Image to Container Registry  
   The Docker image is pushed to a container registry.

5. Deploy to Kubernetes  
   Kubernetes manifests are applied to deploy the application.

---

## Kubernetes Deployment

The `kubedefs/` directory contains Kubernetes configuration files for:

- Deployment
- Service
- Ingress
- ConfigMaps

Example command to deploy:

```bash
kubectl apply -f kubedefs/
```

---

## Running Locally with Docker Compose

To run the application locally:

```bash
docker-compose up --build
```

This will start the required containers and run the application locally.

---

## Infrastructure Automation

The `ansible/` directory contains Ansible playbooks used to automate:

- Server configuration
- Docker installation
- Kubernetes setup
- Environment provisioning

Example command:

```bash
ansible-playbook playbook.yml
```

---

## Learning Outcomes

Through this project, the following DevOps concepts were implemented:

- Continuous Integration / Continuous Deployment
- Containerization with Docker
- Kubernetes deployment and service management
- Infrastructure automation using Ansible
- CI/CD pipeline creation with Jenkins

---

## Future Improvements

- Add Helm charts for Kubernetes deployments
- Implement monitoring with Prometheus & Grafana
- Add logging with ELK stack
- Automate infrastructure provisioning with Terraform

---
