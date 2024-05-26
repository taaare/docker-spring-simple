Dockerized Spring Boot Application

This project demonstrates a simple Spring Boot application that is containerized using Docker. The application includes a REST controller that returns "Hello, Docker!" when accessed.

Table of Contents
Introduction
Prerequisites
Project Structure
Getting Started
Clone the Repository
Build the Project
Run the Application Locally
Build and Run the Docker Container
Accessing the Application
Docker Commands
License
Introduction
This is a simple Spring Boot application that has been containerized using Docker. The application consists of a single REST endpoint that returns "Hello, Docker!" when accessed.

Prerequisites
Before you begin, ensure you have the following installed on your machine:

Java Development Kit (JDK) 11
Maven
Docker
Project Structure
plaintext
Copy code
DockerDemo
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

Getting Started
Clone the Repository
bash
Copy code
git clone https://github.com/your-username/docker-demo.git
cd docker-demo
Build the Project
Clean and package the project using Maven:

bash
Copy code
mvn clean package
Run the Application Locally
Run the JAR file directly to verify it works:

bash
Copy code
java -jar target/docker-demo-0.0.1-SNAPSHOT.jar
You should see the application start and be accessible at http://localhost:8080.

Build and Run the Docker Container
Build the Docker Image
bash
Copy code
docker build -t my-java-app .
Run the Docker Container
bash
Copy code
docker run -p 8080:8080 my-java-app
Accessing the Application
Once the Docker container is running, open your web browser and navigate to:

http://localhost:8080

You should see the message "Hello, Docker!".

Docker Commands
Here are some useful Docker commands for managing your containers:

List Running Containers:

bash
Copy code
docker ps
Stop a Running Container:

bash
Copy code
docker stop <container_id_or_name>
Remove a Stopped Container:

bash
Copy code
docker rm <container_id_or_name>
View Container Logs:

bash
Copy code
docker logs <container_id_or_name>
Remove the Docker Image:

bash
Copy code
docker rmi my-java-app
License
This project is licensed under the MIT License. See the LICENSE file for details.
