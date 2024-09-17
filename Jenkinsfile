pipeline {
    agent any  // This tells Jenkins to run the pipeline on any available agent

    environment {
        DOCKER_IMAGE = 'helloworldweb'  // Change this to the name of your Docker image
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building Docker Image...'
                script {
                    // Building Docker image from Dockerfile
                    docker.build(env.DOCKER_IMAGE)
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests...'
                // Add commands to run your tests here
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add deployment steps here
            }
        }
    }
}
