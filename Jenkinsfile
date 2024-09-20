pipeline {
    agent any  // This tells Jenkins to run the pipeline on any available agent

    environment {
        DOCKER_IMAGE = 'helloworldweb'  //  this is the name of  Docker image
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
                //
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // 
            }
        }
    }
}
