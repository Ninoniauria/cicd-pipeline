pipeline {
  agent any
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
        }

      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  environment {
    registry = 'ninoniauri/task'
  }
}