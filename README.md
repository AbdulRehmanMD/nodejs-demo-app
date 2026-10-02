# Node.js Demo App – Jenkins CI/CD Pipeline

## Task 2: Create a Simple Jenkins Pipeline for CI/CD

### Objective
Automate the build, testing and Docker image publishing process using Jenkins and Docker.

### Tools Used
- Jenkins
- Docker
- Node.js
- Git and GitHub
- Docker Hub

### Pipeline Stages
1. **Checkout:** Download source code from GitHub.
2. **Install Dependencies:** Install packages using `npm ci`.
3. **Run Tests:** Execute tests using `npm test`.
4. **Build Docker Image:** Build the Docker image.
5. **Push Docker Image:** Publish the image to Docker Hub.

### Docker Image
`abdulrehmanmd/nodejs-demo-app:latest`

### Result
The Jenkins pipeline completed successfully. Application tests passed, the Docker image was built and pushed to Docker Hub, and the application was run locally at `http://localhost:3000`.

### Repository
https://github.com/AbdulRehmanMD/nodejs-demo-app

### Conclusion
This project demonstrates a basic CI/CD workflow using Jenkins, GitHub, Node.js and Docker to automate application testing and image publishing.