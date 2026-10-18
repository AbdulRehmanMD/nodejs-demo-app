# Node.js Demo App — CI/CD with Jenkins and GitHub Actions

## 1. Project Overview

This project demonstrates Continuous Integration and Continuous Delivery (CI/CD) for a Node.js application using Jenkins, GitHub Actions, Docker, and Docker Hub.

The pipelines automate source-code checkout, dependency installation, application testing, Docker image building, and image publishing.

## 2. Objectives

- Automate application testing.
- Build a Docker image for the Node.js application.
- Publish the image to Docker Hub.
- Use GitHub for version control and collaboration.
- Demonstrate CI/CD using Jenkins and GitHub Actions.

## 3. Tools Used

- Node.js
- Git and GitHub
- Jenkins
- GitHub Actions
- Docker
- Docker Hub

## 4. GitHub Actions Workflow

The GitHub Actions workflow is named **Node.js CI/CD Pipeline**.

It runs when code is pushed to the `main` branch.

### Pipeline Steps

1. Check out the repository.
2. Set up Node.js.
3. Install dependencies using `npm ci`.
4. Run tests using `npm test`.
5. Log in to Docker Hub using GitHub repository secrets.
6. Build and push the Docker image.

### Workflow Result

The recorded workflow completed successfully. The dependency installation, test, Docker login, and Docker image build-and-push steps all succeeded.

## 5. Jenkins Pipeline

The Jenkins pipeline automates the following stages:

1. Checkout source code from GitHub.
2. Install dependencies using `npm ci`.
3. Run tests using `npm test`.
4. Build the Docker image.
5. Push the Docker image to Docker Hub.

The previously completed Jenkins run succeeded, and the application was tested locally at `http://localhost:3000`.

## 6. Docker Image

**Image:** `abdulrehmanmd/nodejs-demo-app:latest`

Pull the image:

```bash
docker pull abdulrehmanmd/nodejs-demo-app:latest
```

Run the container:

```bash
docker run -d -p 3000:3000 --name nodejs-demo-app abdulrehmanmd/nodejs-demo-app:latest
```

Open `http://localhost:3000` in your browser. If port 3000 is already occupied, stop the existing container or choose another available host port.

## 7. Repository and Evidence

**GitHub repository:**  
https://github.com/AbdulRehmanMD/nodejs-demo-app

**Docker Hub image:**  
https://hub.docker.com/r/abdulrehmanmd/nodejs-demo-app

Screenshots of successful pipeline runs and application output are included in the repository where available.

## 8. Conclusion

This project demonstrates CI/CD concepts by automating testing, Docker image creation, and image publishing using Jenkins and GitHub Actions. It provides practical experience with version control, containerization, and automated delivery workflows.


## Run with Docker Compose

### Prerequisites
- Docker Desktop
- Docker Compose

### Start the application

Run the following command from the project directory:

```bash
docker compose up -d
```

Open http://localhost:3001 in your browser.

### Check the running container

```bash
docker compose ps
```

### Stop the application

```bash
docker compose down
```

The application uses the Docker Hub image
`abdulrehmanmd/nodejs-demo-app:latest`.
