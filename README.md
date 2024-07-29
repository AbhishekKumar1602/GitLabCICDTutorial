# GitLab CI/CD Tutorial Repository
This repository is designed for the GitLab CI/CD Tutorial and features a demo web application built with Flask. It provides a practical example to help users understand and implement continuous integration and deployment (CI/CD) practices using GitLab.

## Flask Demo Web Application
This demo application is a Flask Web Application designed for cloud-native deployment and containerization, showcasing real-time system monitoring metrics. 

### Features

- **System Information**: Displays CPU, Memory, IO, and Process Information, offering insights into system performance and resource utilization.
- **Cloud-Native Design**: Optimized for deployment in Docker containers, Kubernetes clusters, and AWS environments.
- **CI/CD**: Integrated with GitLab CI/CD for automated builds, testing, and deployments, demonstrating practical CI/CD implementation.

## Installation and Setup

### Prerequisites

- **Operating System**: Linux, WSL, or MacOS
- **Python**: Version 3.8 or Higher
- **Docker**: Required for Containerization
- **AWS CLI**: Needed for Deployment to AWS

## Steps to Run Locally

### 1. Clone the Repository
   ```bash
   git clone https://github.com/AbhishekKumar1602/GitLabCICDTutorial
   ```

### 2. Makefile Commands
- `make help`: Displays available commands and their descriptions.
- `make lint`: Lints code without attempting to fix issues.
- `make lint-fix`: Lints code and automatically attempts to fix issues.
- `make image`: Builds the Docker container image.
- `make push`: Pushes the Docker image to a container registry.
- `make run`: Runs the Flask server locally for development and testing.
- `make deploy`: Deploys the application to AWS.
- `make undeploy`: Removes the application from AWS.
- `make test`: Executes unit tests to validate the application.
- `make test-report`: Runs unit tests and generates a detailed report.
- `make test-api`: Performs integration API tests to ensure API functionality.
- `make clean`: Cleans up the project directory, removing temporary and build files.

### 3. Docker Commands
   - **Run Container**:
     ```bash
     docker run --rm -it -p 5000:5000 abhishekkumar1602/flask-demo-web-application:latest
     ```
     Runs the Docker container and maps port 5000 on the host to port 5000 in the container.

   - **Build Container**:
     ```bash
     make image IMAGE_REPO=your-repo IMAGE_TAG=your-tag
     ```
     Builds the Docker container image with the specified repository and tag.

## Deployment

### 1. Kubernetes
   - **Helm Deployment**: Detailed instructions for deploying to Kubernetes using Helm are provided in `deploy/kubernetes/README.md`.

### 2. AWS
   - **ECS (Elastic Container Service)**: Deploy the application to Amazon ECS using the AWS CLI. Ensure ECS configurations and task definitions are properly set up for deployment.
   - **Elastic Beanstalk**: Alternatively, deploy the application to AWS Elastic Beanstalk. Use `make deploy` to automate the deployment to Elastic Beanstalk with the appropriate configurations.
