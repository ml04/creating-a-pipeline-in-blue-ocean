pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'selenium-hub'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

  }
}