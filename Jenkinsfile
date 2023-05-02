pipeline {
  agent any
  
    environment {
        PATH = "${PATH}:/opt/homebrew/bin/npm"
    }
    
  stages {
    stage('Checkout') {
      steps {
        script {
          checkout scm
        }

      }
    }

    stage('Build') {
      steps {
        script {
          sh 'chmod +x ./scripts/build.sh'
          sh './scripts/build.sh'
        }

      }
    }

  }
  environment {
    registry = 'ninoniauri/task'
  }
}



