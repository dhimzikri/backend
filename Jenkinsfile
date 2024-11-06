pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/dhimzikri/backend.git'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                // Replace with your deployment steps, such as:
                // Deploying to a server using SSH or a deployment tool
                // Deploying to a cloud platform like AWS, GCP, or Azure
                sh 'ssh user@host "cd /path/to/deploy && git pull"'
            }
        }
    }
}
