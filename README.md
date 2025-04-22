# CI/CD Pipeline for a Simple Node.js App using Jenkins

This project demonstrates a basic CI/CD pipeline for a Node.js application using Jenkins.

## Project Structure

```
ci-cd-node-app/
├── app.js
├── package.json
├── test/
│   └── app.test.js
├── Jenkinsfile
└── README.md
```

## Application Details

A simple Node.js application that displays "Hello, World!" with a basic test to verify functionality.

## Jenkins Pipeline

The Jenkinsfile defines a pipeline with the following stages:

1. **Clone Code** - Pulls the code from GitHub repository
2. **Install Dependencies** - Installs required npm packages
3. **Run Tests** - Executes the test script
4. **Deploy (Simulation)** - Simulates a deployment process

## Setup Instructions

### 1. Push Code to GitHub

1. Create a new GitHub repository
2. Replace the URL in the Jenkinsfile with your repository URL:
   ```
   git 'https://github.com/your-username/ci-cd-node-app.git'
   ```
3. Push the code to your repository

### 2. Set Up Jenkins

1. Install Jenkins locally by following the [Jenkins Installation Guide](https://www.jenkins.io/doc/book/installing/)
2. Access Jenkins at http://localhost:8080
3. Install the suggested plugins during setup
4. Create a new Pipeline project
5. Configure the Pipeline:
   - Choose "Pipeline script from SCM"
   - Select Git as SCM
   - Enter your repository URL
   - Set the Script Path to "Jenkinsfile"
6. Save and run the pipeline

### 3. Run the Application

After the pipeline completes successfully, you can run the application locally:

```
npm install
npm start
```

## Expected Output

When you run the Jenkins pipeline, you should see:
- Jenkins pulling code from your repository
- Installing npm dependencies
- Running the test
- Simulating deployment

The application itself will output "Hello, World!" when run locally.