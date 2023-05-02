pipeline {
  agent any
  
  environment {
    registry = 'ninoniauri/task'
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



