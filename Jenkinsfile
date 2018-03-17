pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build'
      }
    }
    stage('Test') {
      parallel {
        stage('test_1') {
          steps {
            sleep 10
          }
        }
        stage('test_2') {
          steps {
            sleep 10
          }
        }
        stage('test_3') {
          steps {
            sleep 10
          }
        }
      }
    }
    stage('Report') {
      steps {
        echo 'report'
      }
    }
  }
}