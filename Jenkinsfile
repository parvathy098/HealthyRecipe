pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir('HealthyRecipe') { // Add this line
                    sh 'npm install'
                }
            }
        }
        stage('Test') {
            ssteps {
                dir('HealthyRecipe') { // Add this line
                    sh 'npm test'
                }
            }
         }
    }
}
