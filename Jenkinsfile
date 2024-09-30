pipeline {
    agent any

    environment {
        IMAGE_NAME = "parvathykrishna/healthy-recipe"
        IMAGE_VERSION = "latest"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/parvathy098/healthy-recipe.git'
            }
        }

        stage('Build') {
            steps {
                script {
                    // Build Docker image
                    sh 'docker build -t ${IMAGE_NAME}:${IMAGE_VERSION} .'
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution finished.'
        }
    }
}
