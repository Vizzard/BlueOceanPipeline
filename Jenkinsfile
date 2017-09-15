pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        timeout(time: 10, unit: 'MINUTES') {
          sh 'echo \'long running build\''
        }
        
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
      when {
        environment name: 'READY_TO_DEPLOY', value: 'yes'
      }
      steps {
        echo 'My Deploy'
      }
    }
  }
  post {
    always {
      echo 'I have finished'
    }
    success {
      echo 'I succeeded!'
    }
  }
  environment {
    MyEnv = 'hello'
    READY_TO_DEPLOY = 'yes'
  }
  options {
    timestamps()
  }
}
