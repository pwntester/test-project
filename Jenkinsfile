pipeline {
  agent any
  stages {
    stage('asdf') {
      steps {
        input(message: 'asdf', id: 'asdf', ok: 'asdf', parameters: [file(name: '/etc/passwd')])
      }
    }

  }
}
