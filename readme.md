# Backend ShopApp GitOps CI/CD Pipeline

This project demonstrates how to implement a GitOps Continuous Integration and Continuous Deployment (CI/CD) pipeline for a ASP.NET Web API application. The pipeline automates the process of building the application, analyzing code quality, creating Docker images, scanning Docker images, and deploying the application to a Kubernetes cluster. Argo CD follows the GitOps approach by syncing deployment changes from GitHub to Kubernetes automatically. This helps reduce manual work, improve code quality, increase security, and make deployments faster and more reliable.

<p align="center">
  <a href="">
    <img src="https://i.postimg.cc/nh1s7TMp/gitops-cicd-drawio.png" alt="GitOps CI/CD Pipeline">
  </a>
</p>

## Tech Stack

- GitHub
- Jenkins
- SonarQube
- Trivy
- Docker
- Harbor
- Argo CD
- Kubernetes

## CI/CD Workflow

1. The developer writes code and pushes it to the GitHub repository.

2. Jenkins starts the CI pipeline automatically when it detects a new commit.

3. Jenkins builds the BackendShop application and checks that the project can be built successfully.

4. SonarQube analyzes the source code to find bugs, code smells, and security issues.

5. Trivy scans the Docker image for security vulnerabilities.

6. Jenkins builds a new Docker image and pushes it to the Harbor registry.

7. Jenkins updates the Kubernetes deployment manifest with the new image tag and pushes the change to the Manifest repository on GitHub.

8. Argo CD monitors the Manifest repository. When it detects the new commit, it syncs the changes to the Kubernetes cluster automatically.

9. Kubernetes pulls the new Docker image from Harbor and updates the application with the latest version.

This workflow helps automate the build and deployment process. It also improves code quality, increases security, and makes deployments faster and more reliable.
