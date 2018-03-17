pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build'
      }
    }
    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test'
          }
        }
        stage('test_2') {
          steps {
            echo 'test 2'
          }
        }
        stage('test_3') {
          steps {
            echo 'test_3'
            sleep 10
          }
        }
      }
    }
  }
}