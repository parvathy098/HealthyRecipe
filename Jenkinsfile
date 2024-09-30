pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir('HealthyRecipe') {  // Ensure Jenkins navigates to the correct directory
                    sh 'npm install'
                }
            }
        }
        stage('Test') {
            steps {
                dir('HealthyRecipe') {  // Run npm test from the same directory
                    sh 'npm test'
                }
            }
        }
        stage('Code Quality') {
    steps {
        withSonarQubeEnv('SonarQubeServer') {
            sh 'sonar-scanner'
        }
    }
}

    }
}
