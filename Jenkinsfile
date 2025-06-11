pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        bat 'docker build -t angelocapone/model:v1 .'
      }
    }

    stage('Push') {
      steps {
        bat 'docker push angelocapone/model:v1'
      }
    }
  }
  post {
    always {
      cleanWs() // Pulisce la workspace
    }
  }
}
