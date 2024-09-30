pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from your Git repository
                git branch: 'main', url: 'https://github.com/parvathykrishna/healthy-recipe.git'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline execution finished.'
        }
    }
}
