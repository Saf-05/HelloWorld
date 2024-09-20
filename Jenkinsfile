pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'helloworld'
        DOCKER_TAG = 'latest'
    }

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Saf-05/HelloWorld.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    // This will build your Docker image
                    def dockerImage = docker.build("${DOCKER_IMAGE}:${DOCKER_TAG}")
                }
            }
        }

        stage('Print Docker Image') {
            steps {
                script {
                    // This will print the name and tag of your Docker image
                    echo "Built Docker Image: ${DOCKER_IMAGE}:${DOCKER_TAG}"
                }
            }
        }

        // Add other stages as needed
    }
}
