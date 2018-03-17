pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build'
        sleep 10
      }
    }
    stage('Test') {
      parallel {
        stage('test_1') {
          steps {
            node(label: 'test') {
              echo "test 1 runs ..."
              sleep 10
              echo "... test 1 done"
            }            
          }
        }
        stage('test_2') {
          steps {
            node(label: 'test') {
              echo "test 2 runs ..."
              sleep 10
              echo "... test 2 done"
            }
          }
        }
        stage('test_3') {
          steps {
            node(label: 'test') {
              echo "test 3 runs ..."
              sleep 10
              echo "... test 3 done"
            }
          }
        }
      }
    }
    stage('Report') {
      steps {
        echo 'report'
        sleep 10
      }
    }
  }
}
