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
            node(label: 'test') {
              sleep 10
              writeFile(file: 'report.txt', text: 'test successful')
            }
            
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