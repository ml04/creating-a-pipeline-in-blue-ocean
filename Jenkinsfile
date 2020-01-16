pipeline {
  agent any
  stages {
    stage('Build ') {
      steps {
        echo 'docker:build image of the application'
      }
    }

    stage('Docker-compose') {
      parallel {
        stage('Docker-compose 1') {
          steps {
            echo 'Run docker-compose up that uses a previously built app image'
          }
        }

        stage('Docker-compose 2') {
          steps {
            echo 'Run docker-compose up that uses a previously built app image'
            echo 'X'
          }
        }

        stage('Docker-compose 3') {
          steps {
            echo 'Run docker-compose up that uses a previously built app image'
          }
        }

      }
    }

    stage('Test') {
      parallel {
        stage('HIGH Test') {
          steps {
            echo 'Run a set of High BDD tests'
          }
        }

        stage('MED Test') {
          steps {
            echo 'Run a set of MED BDD tests'
          }
        }

        stage('LOW Test') {
          steps {
            echo 'Run a set of Low BDD tests'
          }
        }

      }
    }

  }
}
