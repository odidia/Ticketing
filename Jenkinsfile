pipeline {
  agent any
  stages {
    stage('Checkout-Code') {
      steps {
        git(url: 'https://github.com/odidia/Ticketing.git', branch: 'main')
      }
    }

    stage('Log') {
      steps {
        sh 'mkdir ticket-frontend ticketbackend && ls -la '
      }
    }

    stage(' Deploy ') {
      steps {
        sh 'docker build -f ticking-frontend/Dockerfile . '
      }
    }

  }
}