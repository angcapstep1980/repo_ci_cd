pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'docker build -t angelocapone/model:v1 .'
      }
    }

    stage('Push') {
      steps {
        sh 'docker push angelocapone/model:v1'
      }
    }
  }
  post {
    always {
      cleanWs() // Pulisce la workspace
    }
  }
}
