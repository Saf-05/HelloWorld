pipeline {
    agent any  

    environment {
        DOCKER_IMAGE = 'helloworldweb'  // name of Docker image
    }

    stages {
        stage('Check for Tag') {
            steps {
                script {
                    // Check if the current build is triggered by a tag
                    if (env.GIT_BRANCH ==~ /refs\/tags\/.*/) {
                        echo "Build triggered by tag: ${env.GIT_BRANCH}"
                    } else {
                        echo "No tag found, skipping the build."
                        currentBuild.result = 'SUCCESS'
                        return // Exit the pipeline if it's not a tag
                    }
                }
            }
        }

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
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
