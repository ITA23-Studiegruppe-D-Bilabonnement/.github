# Bilabonnement Microservices Project
A scalable API application for car rentals using microservices architecture.

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

1. **Customer Microservice**: Handles customer profiles and personal data.
2. **Cars Microservice**: Manages car inventory and availability.
3. **Subscription Microservice**: Tracks subscriptions, rental plans, and billing.
4. **Damage Report Microservice**: Records and processes damage reports.

All services are connected through an **API Gateway**, which routes requests to the appropriate microservices.

### Architecture Diagram
![Architecture Diagram](path/to/architecture_diagram.png)

## Technologies Used
- **Programming Language**: Python
- **Framework**: Flask, Gunicorn, Bcrypt, Flasgger
- **Database**: SQLite3
- **Authentication**: Flask-Extended-JWT
- **Containerization**: Docker
- **Deployment**: Azure
- **Version Control**: GitHub

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
![CI/CD Pipeline](path/to/ci-cd-diagram.png)

## Contributors
- [Lucas Jacobsen](https://github.com/LucasFJ-2023)
- [Christine Tofft](https://github.com/christinetofft)
- [Rasmus Planteig](https://github.com/Planteig1)

