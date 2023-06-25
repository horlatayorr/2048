pipeline {
  agent any
  
  stages {
    stage('Checkout') {
      steps {
        // Checkout the source code from your Git repository
        checkout scm
      }
    }
    
    stage('Build') {
      steps {
        // Install dependencies (if any)
        sh 'npm install'
        
        // Compile SCSS to CSS
        sh 'sass src/styles/main.scss:dist/css/main.css'
        
        // Concatenate and minify JavaScript files
        sh 'uglifyjs src/scripts/*.js -o dist/js/main.min.js'
        
        // Copy HTML files to the dist directory
        sh 'cp src/*.html dist/'
        
        // Copy additional static assets (images, fonts, etc.)
        sh 'cp -R src/assets dist/'
      }
    }

  stage('Test') {
    steps {
        sh 'npm run test' // Run tests
      }
    }
        
  stage('Deploy') {
    steps {
        echo "deploying..."
      }
    }
  
  
  }
}
