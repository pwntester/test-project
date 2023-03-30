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

    stage('asdf') {
      steps {
        input(message: 'asdf', id: 'asdf', ok: 'asdf', parameters: [
                            file(name: '/etc/passwd')
                        ])
      }
    }

  }
}
