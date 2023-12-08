pipeline {
    agent any
    stages {
        stage('Install Dependencies') {
            steps {
                script {
                    // Install necessary dependencies
                    sh 'npm install'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    // Build your Svelte application
                    sh 'npm run build'
                    // Build your Docker image
                    sh 'docker build -t your-image-name:latest .'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Deploy your Docker container
                    sh 'docker stop your-container-name || true'
                    sh 'docker rm your-container-name || true'
                    sh 'docker run -d --name your-container-name your-image-name:latest'
                }
            }
        }
    }
}
