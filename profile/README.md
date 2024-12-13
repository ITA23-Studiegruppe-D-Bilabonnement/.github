![Python](https://img.shields.io/badge/Python-3.9-blue) 
![Flask](https://img.shields.io/badge/Flask-2.0-blue) 
![Gunicorn](https://img.shields.io/badge/Gunicorn-Enabled-blue) 
![Bcrypt](https://img.shields.io/badge/Bcrypt-Enabled-blue) 
![Flasgger](https://img.shields.io/badge/Flasgger-Enabled-blue) 
![SQLite3](https://img.shields.io/badge/SQLite3-v3.36.0-blue) 
![Docker](https://img.shields.io/badge/Docker-Enabled-blue) 
![Azure](https://img.shields.io/badge/Azure-Enabled-blue)
# Bilabonnement Microservices Project
A scalable API application for car rentals using microservices architecture.

## Table of Contents
- [About the Project](#about-the-project)
- [Architecture Overview](#architecture-overview)
- [CI/CD Pipeline](#cicd-pipeline)
- [Project Management](#project-management)
- [Technologies Used](#technologies-used)
- [Contributors](#contributors)

## About the Project
Bilabonnement is a car rental company that allows customers to rent cars on a subscription basis. 
For our exam project, we were tasked with creating an API application to manage the company's core functionalities using a microservices architecture.

### Objectives
- Develop a modular and scalable system to handle the company's operations.
- Ensure clear separation of concerns between different functionalities.

### Features
- Customer management: Register and manage customer profiles.
- Car inventory: Keep track of available cars.
- Subscription handling: Manage rental plans and customer subscriptions.
- Damage reporting: Log and manage damage reports for rented cars.
- API Gateway: Centralized routing for all microservices.


## Architecture Overview
The application is built using a microservices architecture, divided into the following services:

1. Customer Microservice: Handles customer profiles and personal data.
   - [**Github Repository**](https://github.com/ITA23-Studiegruppe-D-Bilabonnement/Customer-microservice)
   - [**Azure**](https://portal.azure.com/#@stud.kea.dk/resource/subscriptions/fa4e99f2-bbe7-4cca-b3ca-46e70febed28/resourceGroups/Eksamensprojekt-BIlabonnement/providers/Microsoft.Web/sites/Customer-microservice/appServices)
   - [**Hosted Microservice**](https://customer-microservice-b4dsccfkbffjh5cv.northeurope-01.azurewebsites.net)
   - [**DockerHub Repository**](https://hub.docker.com/r/planteig/customer-microservice)
2. Cars Microservice: Manages car inventory and availability.
   - [**Github Repository**](https://github.com/ITA23-Studiegruppe-D-Bilabonnement/Cars-microservice)
   - [**Azure**](https://portal.azure.com/#@stud.kea.dk/resource/subscriptions/fa4e99f2-bbe7-4cca-b3ca-46e70febed28/resourceGroups/Eksamensprojekt-BIlabonnement/providers/Microsoft.Web/sites/Cars-microservice/appServices)
   - [**Hosted Microservice**](https://cars-microservice-a7g2hqakb2cjffef.northeurope-01.azurewebsites.net)
   - [**DockerHub Repository**](https://hub.docker.com/r/planteig/cars-microservice)
3. Subscription Microservice: Tracks subscriptions, rental plans.
   - [**Github Repository**](https://github.com/ITA23-Studiegruppe-D-Bilabonnement/Subscription-microservice)
   - [**Azure**](https://portal.azure.com/#@stud.kea.dk/resource/subscriptions/fa4e99f2-bbe7-4cca-b3ca-46e70febed28/resourceGroups/Eksamensprojekt-BIlabonnement/providers/Microsoft.Web/sites/Subscription-microservice/appServices)
   - [**Hosted Microservice**](https://subscription-microservice-gxbuenczgcd5hfe4.northeurope-01.azurewebsites.net)
   - [**DockerHub Repository**](https://hub.docker.com/r/planteig/subscription-microservice)
4. Damage Report Microservice: Records and processes damage reports.
   - [**Github Repository**](https://github.com/ITA23-Studiegruppe-D-Bilabonnement/Damage-report-microservice)
   - [**Azure**](https://portal.azure.com/#@stud.kea.dk/resource/subscriptions/fa4e99f2-bbe7-4cca-b3ca-46e70febed28/resourceGroups/Eksamensprojekt-BIlabonnement/providers/Microsoft.Web/sites/damagereport-microservice/appServices)
   - [**Hosted Microservice**](https://damagereport-microservice-gpfchac2c4c9hzdc.northeurope-01.azurewebsites.net)
   - [**DockerHub Repository**](https://hub.docker.com/r/planteig/damagereport-microservice)

All services are connected through an API-Gateway, which routes requests to the appropriate microservices.
   - [**Github Repository**](https://github.com/ITA23-Studiegruppe-D-Bilabonnement/API-gateway)
   - [**Azure**](https://portal.azure.com/#@stud.kea.dk/resource/subscriptions/fa4e99f2-bbe7-4cca-b3ca-46e70febed28/resourcegroups/Eksamensprojekt-BIlabonnement/providers/Microsoft.Web/sites/API-gatewayservice/appServices)
   - [**Hosted Gateway**](https://api-gatewayservice-cbc0dydhctg9g0hk.northeurope-01.azurewebsites.net)
   - [**DockerHub Repository**](https://hub.docker.com/r/planteig/api-gatewayservice)

### Architecture Diagram
![Architecture Diagram](https://github.com/ITA23-Studiegruppe-D-Bilabonnement/.github/blob/cab92c4659e9e3df3c68fee52ff1bae972b7b31f/Arkitekturdiagram%20v2.png)

## CI/CD Pipeline

As part of the project, we implemented a CI/CD pipeline to automate the deployment process. The pipeline includes the following steps:

1. **Code Editing and Version Control**:
   - Changes are made locally in the editor and pushed to GitHub.

2. **Docker Image Build**:
   - On every push to the main branch, the Docker image for the project is built.

3. **Docker Hub Integration**:
   - The built image is pushed to Docker Hub, ensuring easy access for deployment.

4. **Deployment to Azure**:
   - Azure pulls the Docker image from Docker Hub and deploys it to Azure services, making the application available for use.

### Pipeline Diagram
![CI/CD Pipeline](https://github.com/ITA23-Studiegruppe-D-Bilabonnement/.github/blob/cab92c4659e9e3df3c68fee52ff1bae972b7b31f/Deployment%20process.png)

## Project Management

We followed the Scrum framework to manage the development process. This included:
- **Sprint Planning**: Breaking down tasks into smaller deliverables.
- **Daily Standups**: Coordinating team efforts and resolving blockers.
- **Retrospectives**: Reviewing progress and identifying areas for improvement.

Scrum allowed us to maintain focus on iterative development and ensure continuous delivery throughout the project.

## Sprint Progress

### Burndown Charts

Below are the burndown charts showing the progress of the project during the development sprints.

#### Sprint 1
- **Goal**: 213 story points
- **Achievement**: Reached 25 story points on the last day, still short of the goal.

![Sprint 1 Burndown](https://github.com/ITA23-Studiegruppe-D-Bilabonnement/.github/blob/a6455d506332c9d50bfbf6e7464ba5cffc6868ce/Sprint%201%20(%20Burndown%20chart%20).png)

#### Sprint 2
- **Goal**: 263 story points
- **Achievement**: Fully achieved the goal (0 story points remaining).

![Sprint 2 Burndown](https://github.com/ITA23-Studiegruppe-D-Bilabonnement/.github/blob/a6455d506332c9d50bfbf6e7464ba5cffc6868ce/Sprint%202%20(%20Burndown%20chart%20).png)


### Velocity Overview
- **Sprint 1 Velocity**: 188 story points  
- **Sprint 2 Velocity**: 263 story points  
- **Average Velocity**: 225.5 story points per sprint

## Technologies Used
- **Programming Language**: Python
- **Frameworks**
   - Flask
   - Gunicorn
   - Bcrypt
   - Flasgger
- **Database**: SQLite3
- **Authentication**: Flask-Extended-JWT
- **Containerization**: Docker
- **Deployment**: Azure
- **Version Control**: GitHub


## Contributors
- [Lucas Jacobsen](https://github.com/LucasFJ-2023)
- [Christine Tofft](https://github.com/christinetofft)
- [Rasmus Planteig](https://github.com/Planteig1)

