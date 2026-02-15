## Containerized Static Website Deployment with CI/CD to AWS ECR
Project Overview

This project demonstrates the end-to-end containerization and automated delivery of a static HTML medical directory website (Mediplus template) using Docker and GitHub Actions CI/CD, with image publishing to Amazon Elastic Container Registry (ECR).

The objective of this implementation is to eliminate manual deployment processes and establish a repeatable, production-aligned CI/CD workflow.

This repository showcases practical DevOps engineering skills, including:

Docker containerization

GitHub Actions workflow automation

Secure AWS authentication using IAM credentials

Automated image build and push to AWS ECR

Infrastructure-independent deployment architecture

Architecture Overview

The delivery pipeline follows this automated workflow:

Developer Push
↓
GitHub Actions Trigger
↓
Docker Image Build
↓
Authentication to AWS
↓
Image Push to Amazon ECR

No manual Docker builds.
No local image tagging.
No direct registry interaction.

All delivery is pipeline-driven.

Technologies Used

HTML5 / CSS3 (Static Website)

Docker

GitHub Actions

AWS ECR

IAM (Secure access control)

CI/CD Automation

Key DevOps Implementations
1. Docker Containerization

Created production-ready Dockerfile

Lightweight container build

Reproducible environment

Consistent image tagging strategy

2. CI/CD Pipeline (GitHub Actions)

Triggered on push to main branch

Automated Docker image build

Secure AWS credential injection via GitHub Secrets

ECR login using AWS CLI

Image push to AWS ECR repository

3. Secure Credential Management

No hardcoded secrets

AWS Access Key stored in GitHub Secrets

Least-privilege IAM configuration

Token-based registry authentication

Security Practices Applied

Secrets managed via GitHub encrypted secrets

No credentials stored in the repository

Controlled execution through a branch-based trigger

Registry authentication is performed during pipeline runtime only

Why This Project Matters

This implementation reflects real-world DevOps practices:

Infrastructure-independent deployments

Pipeline-first delivery model

Reproducible builds

Secure container publishing

Elimination of manual deployment risk

It demonstrates practical experience in container lifecycle management and CI/CD automation — core competencies required in modern DevOps and Cloud Engineering roles.

Repository Structure
.github/workflows/   → CI/CD workflow definition
Dockerfile           → Container build configuration
index.html           → Static website entry point
css/                 → Styles
js/                  → Scripts
img/                 → Static assets

Future Enhancements

Deployment to Amazon ECS or EKS

Blue/Green deployment strategy

Image scanning integration

Version tagging strategy

Infrastructure as Code for full-stack automation

Author

Cloud & DevOps Engineer
Focused on production-grade automation, infrastructure as code, and secure delivery pipelines.
