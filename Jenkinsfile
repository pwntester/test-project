pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        sh '''pwd

'''
      }
    }

    stage('another') {
      steps {
        echo 'asdfasdf'
      }
    }

    stage('input') {
      steps {
        input(message: 'Hello', id: 'ID', ok: 'OK')
      }
    }

  }
}