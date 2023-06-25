pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Clone the repository
                checkout scm
                
                // Build the game app
                sh 'npm install'
                
            }
        }
        
        stage('Test') {
            steps {
                // Run tests for the game app (if applicable)
                // Modify the test command as per your project requirements
                sh 'npm run tests'
                sh 'echo "No tests"'
            }
        }
        
        stage('Deploy') {
            steps {
                echo "deploying..."
            }
        }
    }
}
