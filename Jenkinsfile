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
        input(message: 'dame datos', id: 'dame', ok: 'datos', submitter: 'foo', submitterParameter: 'bar')
      }
    }

  }
}