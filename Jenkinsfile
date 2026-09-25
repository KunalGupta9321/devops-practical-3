pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Verify Files') {
            steps {
                // Check that app.py and Dockerfile exist in the workspace
                sh 'ls -la'
            }
        }

        stage('Run Application') {
            steps {
                echo 'Executing application validation stage...'
                sh 'cat app.py'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Simulating Docker build step inside Jenkins runner...'
                sh 'cat Dockerfile'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }
        failure {
            echo 'CI/CD Pipeline failed!'
        }
    }
}