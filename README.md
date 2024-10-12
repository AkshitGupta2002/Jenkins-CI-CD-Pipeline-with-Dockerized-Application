# 🚀 CI/CD Pipeline with Jenkins, SonarQube, and Docker

This repository contains the codebase for a continuous integration and continuous deployment (CI/CD) pipeline using Jenkins, SonarQube, and Docker.

## Overview

The pipeline is triggered automatically whenever there is a code commit to the repository. It performs the following steps:
1. 🛠️ **Trigger Jenkins Pipeline**: A webhook is configured to trigger the Jenkins pipeline when there is a new commit in the GitHub repository.
2. 🔍 **SonarQube Analysis**: Jenkins runs a SonarQube analysis to check for vulnerabilities, code quality issues, and code coverage.
3. 🐳 **Docker Containerization**: Once the SonarQube analysis is completed, Jenkins builds a Docker image of the application.
4. 🚢 **Deployment**: The Docker container is deployed, making the application ready for use.

## 📜 Pipeline Workflow

1. 🔗 **GitHub Webhook**: Set up a webhook in your GitHub repository to trigger the Jenkins pipeline on every push or pull request.
2. 🏗️ **Jenkins Pipeline**: The `Jenkinsfile` defines the stages of the CI/CD pipeline.
   - 📦 **Clone Repository**: Fetches the latest code from the repository.
   - 🔍 **SonarQube Scan**: Runs SonarQube analysis to check for code vulnerabilities.
   - 🐳 **Build Docker Image**: Builds the Docker image of the application using the `Dockerfile`.
   - 🚀 **Deploy**: Deploys the application inside a Docker container.

## 📂 Files

- **`Jenkinsfile`**: Defines the Jenkins pipeline, including stages for SonarQube analysis, Docker build, and deployment.
- **`Dockerfile`**: Contains the instructions for building the Docker image of the application.
- **Application Code**: The source code for the application.

## ✅ Prerequisites

- 🧑‍💻 **Jenkins**: A Jenkins server set up with GitHub integration and Docker installed.
- 📊 **SonarQube**: A SonarQube server for code analysis and vulnerability checks.
- 🐳 **Docker**: Docker installed on the Jenkins server to build and run containers.
- 🔗 **GitHub Webhook**: Configured to trigger the Jenkins pipeline on code changes.

## 🚀 Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/your-repo.git
   ```
2. Ensure that the Jenkins and the SonarQube are properly integrated
3. Push the code changes to trigger the pipeline automatically

   ```bash
   git add .
   git commit -m "Your commit message"
   git push -u origin main
   ```
4. Jenkins will run the pipeline, show code analysis results from SonarQube, build the Docker image, and deploy the application.

