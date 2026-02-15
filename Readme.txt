# Containerized Static Website with CI/CD to AWS ECR

## 📌 Project Overview

This project demonstrates the containerization and automated delivery of a static HTML website using Docker and GitHub Actions.

The application is a static medical directory website (Mediplus template) packaged into a Docker image and automatically built and pushed to Amazon Elastic Container Registry (ECR) through a CI/CD pipeline.

This setup eliminates manual builds and ensures reproducible, automated deployments.

---

## 🏗 Architecture Overview

The delivery pipeline follows this flow:

Developer Push  
⬇  
GitHub Actions Trigger  
⬇  
Docker Image Build  
⬇  
Image Push to AWS ECR  
⬇  
Container Image Ready for Deployment  

---

## 🧱 Project Structure



.
├── .github/
│ └── workflows/
│ └── cicd.yml
├── css/
├── js/
├── img/
├── index.html
├── portfolio-details.html
├── contact.html
├── Dockerfile
└── README.md


---

## 🚀 Key Features

- Static website built with HTML, CSS, and JavaScript
- Dockerized for portability and consistency
- GitHub Actions CI/CD pipeline
- Automated Docker image build on push
- Secure image push to AWS ECR
- No manual Docker builds or pushes
- Secrets managed through GitHub repository secrets

---

## 🐳 Docker Configuration

The Dockerfile packages the static site into a lightweight web server container.

Example structure:

```dockerfile
FROM nginx: alpine
COPY. /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]


This ensures:

Lightweight image

Fast build time

Simple static file serving

Production-ready base image

⚙️ CI/CD Pipeline

The GitHub Actions workflow performs the following:

Checks out the repository

Configures AWS credentials

Logs in to Amazon ECR

Builds Docker image

Tag the image with commit SHA or latest

Pushes image to ECR

Trigger:

On push to main branch

This enforces automation and consistency in image builds.

🔐 Security Practices

AWS credentials stored as GitHub Secrets

No hardcoded credentials

Controlled branch-based deployment

Immutable container images

📦 Technologies Used

HTML / CSS / JavaScript

Docker

GitHub Actions

AWS ECR

NGINX (Alpine)

🎯 What This Project Demonstrates

Infrastructure automation mindset

CI/CD pipeline design

Containerization best practices

Secure credential management

Cloud registry integration

Production-ready delivery workflow

🛠 Future Improvements

Deploy image to ECS or EKS

Add multi-stage Docker builds

Implement image vulnerability scanning

Add an automated testing stage

Add staging and production environments

## Author

Built as part of a DevOps portfolio demonstrating containerized application delivery and CI/CD pipeline automation.


---

## Why This README Is Strong

This version:

- Explains architecture
- Shows DevOps thinking
- Mentions security
- Highlights automation
- Speaks in recruiter-friendly language
- Avoids beginner tone
- Focuses on engineering decisions
