pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building ..... Pipeline'
      }
    }
    stage('Test') {
      parallel {
        stage('Test Firefox') {
          steps {
            sh 'echo \'Testing FireFox\''
          }
        }
        stage('Test Chrome') {
          steps {
            sh 'echo \'Testing Chrome\'; exit 1'
          }
        }
        stage('Test Edge') {
          steps {
            sh 'echo \'Testing Edge\''
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying ... PipeLIne'
      }
    }
  }
}
