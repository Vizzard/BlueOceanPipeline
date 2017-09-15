pipeline {
  agent any
  
 // using the Timestamper plugin we can add timestamps to the console log
 options {
   timestamps()
 }

  stages {
    stage('Build') {
      steps {
        echo 'Build Step'
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
}
