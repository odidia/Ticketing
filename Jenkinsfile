pipeline {
  agent any
  stages {
    stage('Checkout-Code') {
      steps {
        git(url: 'https://github.com/odidia/Ticketing.git', branch: 'main')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh 'ls -la '
          }
        }

        stage('Front-End Unit Tests') {
          steps {
            sh 'mkdir ticketing-frontend ticketing-backend && cd ticketing-frontend  && sudo yum update && sudo yum run test:unit '
          }
        }

      }
    }

  }
}