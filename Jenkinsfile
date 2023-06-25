pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Clone the repository
                checkout scm
                
                // Build the game app
                sh 'npm install -g http-server'
                sh 'npm install -g sass'
                sh 'sass style/main.scss style/main.css'
                //sh 'cp src/* dist/'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests for the game app (if applicable)
                // Modify the test command as per your project requirements
                sh 'echo "No tests"'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy the game app to a web server or hosting platform
                // Replace the placeholder commands with your deployment process
                sh 'http-server dist'
            }
        }
    }
}
