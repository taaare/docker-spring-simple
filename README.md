# Dockerized Spring Boot Application

This project demonstrates a simple Spring Boot application that is containerized using Docker. The application includes a REST controller that returns "Hello, Docker!" when accessed.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Clone the Repository](#clone-the-repository)
  - [Build the Project](#build-the-project)
  - [Run the Application Locally](#run-the-application-locally)
  - [Build and Run the Docker Container](#build-and-run-the-docker-container)
- [Accessing the Application](#accessing-the-application)
- [Docker Commands](#docker-commands)
- [License](#license)

## Introduction

This is a simple Spring Boot application that has been containerized using Docker. The application consists of a single REST endpoint that returns "Hello, Docker!" when accessed.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- [Java Development Kit (JDK) 11](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
- [Maven](https://maven.apache.org/install.html)
- [Docker](https://www.docker.com/get-started)

## Project Structure

DockerDemo
```
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── example
│   │   │           └── demo
│   │   │               ├── DemoApplication.java
│   │   │               └── HelloController.java
├── target
├── Dockerfile
└── pom.xml
```

## Getting Started

### Clone the Repository

git clone https://github.com/your-username/docker-demo.git
cd docker-demo


## Run the Application Locally
### Run the JAR file directly to verify it works:


java -jar target/docker-demo-0.0.1-SNAPSHOT.jar
You should see the application start and be accessible at http://localhost:8080.

## Build and Run the Docker Container
### Build the Docker Image

docker build -t my-java-app .
Run the Docker Container

docker run -p 8080:8080 my-java-app

## Accessing the Application
Once the Docker container is running, open your web browser and navigate to:

http://localhost:8080

You should see the message "Hello, Docker!".

## Docker Commands
Here are some useful Docker commands for managing your containers:

List Running Containers

docker ps
Stop a Running Container

docker stop <container_id_or_name>
Remove a Stopped Container

docker rm <container_id_or_name>
View Container Logs

docker logs <container_id_or_name>
Remove the Docker Image

docker rmi my-java-app


## License
This project is licensed under the MIT License. See the LICENSE file for details.
