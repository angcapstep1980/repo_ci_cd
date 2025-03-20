pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        bat 'docker build -t angelocapone/model:v3 .'
      }
    }

    stage('Push') {
      steps {
        bat 'docker push angelocapone/model:v3'
      }
    }
  }
  post {
    always {
      cleanWs() // Pulisce la workspace
    }
  }
}
