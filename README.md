About
-
This repository contains source code for a BDBI @ Georgia Tech workshop that covers Docker. We are iterating off of the [previous platform workshop](https://github.com/bdbiworkshops/platform-rest-apis) but focusing on the Docker component.

Installation
-
1. Make sure you have [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed and running
2. Clone the repository with `git clone https://github.com/bdbiworkshops/platform-docker`
3. Fill out `Dockerfile.frontend`, `Dockerfile.python`, and `docker-compose.yaml` (follow along with workshop, source code to be uploaded later)
4. Build the application with `docker-compose up --build`
5. Navigate to http://localhost:8080 to view the website

Architecture
-
This multi-container application is made up of 3 containers:
1. frontend: an nginx web server that hosts a static website and serves as a reverse proxy to the Flask application
2. flask_app: a REST API written in Flask used to communicate with the PostgreSQL database
3. db: a PostgreSQL database