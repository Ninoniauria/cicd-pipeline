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

          sh 'export PATH=/opt/homebrew/bin:$PATH && ./scripts/build.sh'
        }

      }
    }

    stage('Test') {
      steps {
        script {
          sh 'chmod +x ./scripts/test.sh'
          sh 'export PATH=/opt/homebrew/bin:$PATH && ./scripts/test.sh'
        }

      }
    }

    stage('Docker Image Build') {
      steps {
        script {
          sh 'export PATH=/usr/local/bin:$PATH && docker build -t myimage .'
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