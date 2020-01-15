pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'tomcat:8.5.50-jdk8-openjdk'
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