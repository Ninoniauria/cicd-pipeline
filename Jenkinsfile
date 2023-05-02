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
          sh 'cat ./scripts/build.sh'
          sh './scripts/build.sh'
        }

      }
    }

  }
  environment {
    registry = 'ninoniauri/task'
  }
}