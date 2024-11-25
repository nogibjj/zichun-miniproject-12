
# Python Application in Docker

## Overview
This project demonstrates how to containerize a simple Python application using Docker and automate the build and deployment with GitHub Actions.

## Features
- Flask-based API to return the current time.
- Dockerized application with automated builds.
- CI/CD pipeline to push images to Docker Hub.

## How to Run
1. Build the Docker image locally:
   ```bash
   docker build -t my-python-app .
   ```
2. Run the Docker container:
   ```bash
   docker run -p 5000:5000 my-python-app
   ```
3. Access the app at `http://localhost:5000`.

## CI/CD Pipeline
The GitHub Actions workflow automatically builds and pushes the Docker image to Docker Hub on every push to the `main` branch.

## Repository Structure
```
.
├── src/
│   ├── main.py           # Python application logic
├── requirements.txt      # Dependencies
├── Dockerfile            # Docker configuration
├── .github/
│   ├── workflows/
│       ├── ci.yml        # GitHub Actions configuration
├── README.md             # Project documentation
```

## CI/CD Setup
1. Add the following secrets to your GitHub repository:
   - `DOCKER_USERNAME`: Your Docker Hub username.
   - `DOCKER_PASSWORD`: Your Docker Hub password.
2. Modify the `ci.yml` file to include your Docker Hub repository.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
