pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Show me my Build Step'
      }
    }
    stage('Unit Test') {
      steps {
        parallel(
          "Test 01": {
            sleep 5
            echo 'test 01'
            
          },
          "Test 02": {
            sleep 5
            echo 'test 02'
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
  environment {
    MyEnv = 'hello'
  }
  options {
    timestamps()
  }
}