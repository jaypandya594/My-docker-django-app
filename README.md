This project consists of the Docker and Docker Compose files to run a full-stack Django/React notes application in a multi-container environment.

The original application code can be found at https://github.com/LondheShubham153/django-notes-app.git. My work involved containerizing the application and all its services for easy deployment.

  Technology Stack

    Application: Django (Backend) & React (Frontend)

    Containerization: Docker

    Orchestration: Docker Compose

    Database: MySQL

    Reverse Proxy: Nginx

  Features

    Dockerfile: A custom Dockerfile that containerizes the Django application, installing all Python and system dependencies.

  Docker-compose.yml: A single file to build and run all three services:

    django: The Python web application.

    db: The MySQL database.

    nginx: A reverse proxy that serves the application.

Database Configuration: Uses a .env file to securely pass database credentials to the Django and MySQL containers.

    Persistent Data: Uses a Docker volume to ensure that all data in the MySQL database is saved even if the container is stopped or restarted.

 How to Run This Project

    Clone this repository:
    Bash

git clone https://github.com/your-username/docker-django-notes-app.git
cd docker-django-notes-app

Create a .env file: Create a file named .env in the main folder and paste the following content (from the original .env ):

DB_NAME=test_db
DB_USER=root
DB_PASSWORD=root
DB_PORT=3306
DB_HOST=db_cont

Build and Run the Application: Run the following command from your terminal:
Bash

docker-compose up --build -d

This will build the images, create the containers, and start them in the background.

Access the Application: Once it's running, you can access the application in your browser at: http://localhost:80
