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
            sh 'mkdir ticket-frontend ticketbackend && ls -la '
          }
        }

        stage('Front End Unit Tests') {
          steps {
            sh 'cd ticket-frontend && npm i && npm run test:unit '
          }
        }

      }
    }

  }
}