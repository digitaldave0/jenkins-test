pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from Git
                git 'https://github.com/your-repository.git'
            }
        }
        
        stage('Build and Publish Docker Image') {
            steps {
                // Build the Docker image
                script {
                    def dockerImage = docker.build("your-image-name:${env.BUILD_NUMBER}")
                    // Push the Docker image to a registry
                    dockerImage.push()
                }
            }
        }
    }
}

