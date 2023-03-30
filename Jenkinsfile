pipeline {
  agent any
  stages {
    stage('asdf') {
      steps {
        input(message: 'asdf', id: 'asdf', ok: 'asdf', parameters: [base64File(name: 'file', base64: Base64.encoder.encodeToString('pwned'.bytes))])
      }
    }

  }
}
