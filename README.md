# Simple Python Flask Dockerized Application

This is a simple Python Flask application that has been dockerized for easy deployment.

## Prerequisites

- Docker installed on your machine
- Basic knowledge of Docker and Flask

## Building the Docker Image

To build the Docker image, run the following command in the root directory of the project:

```bash
docker build -t simple-flask-app:latest .
```

## Running the Docker Container

To run the Docker container, use the command shown below:

```bash
docker run -d -p 5001:5000 simple-flask-app
```

The application will be accessible at [http://127.0.0.1:5001](http://127.0.0.1:5001).

## Dockerfile Details

The `Dockerfile` used to build the image is as follows:

```dockerfile
FROM python:3.6
MAINTAINER Yashwant Kumar "yashwantmahto@gmail.com"
COPY . /app
WORKDIR /app
EXPOSE 5001
RUN pip install -r requirements.txt
ENTRYPOINT ["python", "app.py"]
```

## Application Details

This application has a single route:

- `/` - Returns a welcome message.

## Environment Variables

- `PORT`: The port on which the Flask application will run (default is `5001`).

## File Structure

```
app.py           # Main application file
Dockerfile       # Docker configuration file
README.md        # This README file
requirements.txt # Python dependencies
```

## Maintainer

Yashwant Kumar Mahto - [yashwantmahto@gmail.com]
