pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/adarshsharma-18/CI-CD_jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test test/app.test.js'
            }
        }

        stage('Deploy (Simulation)') {
            steps {
                echo 'Deployment simulated: Your app is ready!'
            }
        }
    }
}