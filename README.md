# Movie Picture Pipeline

This project implements CI/CD pipelines for the Movie Picture application using GitHub Actions.
The application contains a React frontend and a Flask backend.
The goal of the project is to automate linting, testing, building, and deployment.
Both applications are deployed to Kubernetes on AWS EKS.
Docker images are stored in Amazon ECR.
The pipelines use GitHub Actions workflows for both CI and CD.

The repository includes four workflows:
1. Frontend Continuous Integration
2. Frontend Continuous Deployment
3. Backend Continuous Integration
4. Backend Continuous Deployment

The CI workflows run lint, test, and build jobs.
The CD workflows run lint, test, build, push, and deploy jobs.
Docker images are tagged using the Git commit SHA.
Kubernetes manifests are updated with Kustomize before deployment.

Frontend URL:
http://a02e81a99485d4ea782c3f77f8d93439-1867014374.us-east-1.elb.amazonaws.com

Backend URL:
http://a79a85b57b03b4b7eb71e9ee4744b4de-959565981.us-east-1.elb.amazonaws.com/movies

Note: These endpoints were created during deployment. After cloud resources were restarted, the AWS environment was reprovisioned and the EKS cluster had no available nodes due to an AWS permissions/SCP issue, so the live URLs may no longer respond even though the CI/CD workflows completed successfully.

The frontend displays the movie list from the backend API.
The backend exposes a `/movies` endpoint that returns movie data in JSON format.
This project uses GitHub Actions, Docker, Kubernetes, AWS ECR, and AWS EKS.
The workflows are stored in the `.github/workflows` directory.
The frontend source code is in `starter/frontend`.
The backend source code is in `starter/backend`.
This project demonstrates a complete CI/CD pipeline for a containerized web application.
