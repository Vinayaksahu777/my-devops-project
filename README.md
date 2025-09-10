Flask Docker DevOps Example
A minimal Python Flask web application, containerized with Docker, ready for DevOps CI/CD pipelines and cloud deployment.

Table of Contents

- Project Overview
- Tech Stack
- Setup & Usage
- Docker & Deployment
- CI/CD Pipeline
- License

Project Overview
This repository demonstrates a simple Python Flask API, dockerized and integrated with a GitHub Actions-based CI/CD pipeline. Code pushes trigger the automated build, test, and push of the Docker image to Docker Hub.

Tech Stack
- Python 3.9
- Flask
- Docker
- GitHub Actions

Setup & Usage
1. Clone the repo:
   - git clone https://github.com/vinusahu777/flask-docker-app.git
   - cd flask-docker-app
2. Run locally (for development):
   - pip install flask
   - python app.py
   Visit http://localhost:5000

Docker & Deployment
1. Build the Docker image:
   - docker build -t flask-docker-app .
2. Run the Docker container:
   - docker run -p 5000:5000 flask-docker-app
3. Push to Docker Hub:
   - docker tag flask-docker-app yourusername/flask-docker-app:latest
   - docker push yourusername/flask-docker-app:latest
CI/CD Pipeline
- GitHub Actions workflow file: .github/workflows/ci-cd.yml
- Triggers on main branch push
- Automates:
  - Build & Test
  - Docker image creation
  - Push to Docker Hub
License
- MIT
