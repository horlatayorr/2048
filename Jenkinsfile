pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'npm install' // Install dependencies
                //sh 'npm run build' // Build the application
            }
        }

        stage('Build 2') {
            steps {
                sh 'ng build --prod --aot --sm --progress=false'
            }
        }
            
        stage('Test') {
            steps {
                sh 'npm run test' // Run tests
            }
        }
        
        stage('Deploy') {
            steps {
                echo "Deploying..."
            }
        }

    }
}
