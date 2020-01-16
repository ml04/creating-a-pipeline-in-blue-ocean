pipeline {
  agent any
  stages {
    stage('Build ') {
      steps {
        echo 'docker:build image of the application'
      }
    }

    stage('Docker-compose and test') {
      parallel {
        stage('Compose and test HIGH') {
          stages {
            stage('Docker-compose 1') {
              steps {
                echo 'Run docker-compose up that uses a previously built app image'
              }
            }

            stage('HIGH Test') {
              steps {
                echo 'Run a set of High BDD tests'
              }
            }
          }
        }

        stage('Compose and test MED') {
          stages {
            stage('Docker-compose 2') {
              steps {
                echo 'Run docker-compose up that uses a previously built app image'
                echo 'X'
              }
            }

            stage('MED Test') {
              steps {
                echo 'Run a set of MED BDD tests'
              }
            }
          }
        }

        stage('Compose and test LOW') {
          stages {
            stage('Docker-compose 3') {
              steps {
                echo 'Run docker-compose up that uses a previously built app image'
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

    stage('Deliver') {
      steps {
        echo 'Deliver a tested solution'
      }
    }

  }
}
