pipeline {
  agent {
    docker {
      image 'golang:1.10.1-alpine'
      label 'docker-cloud'
    }
    
  }
  stages {
    stage('Say Hello') {
      steps {
        echo 'Hello "$(MY_NAME)!"'
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
        sh 'go version'
      }
    }
  }
  environment {
    MY_NAME = 'MARY'
    TEST_USER = credentials('test-user')
  }
}