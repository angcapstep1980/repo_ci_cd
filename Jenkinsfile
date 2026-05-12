pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'docker build -t angelocapone/model:v2 .'
      }
    }

    stage('Push') {
      steps {
        sh 'docker push angelocapone/model:v2'
      }
    }
  }
  post {
    always {
      cleanWs() // Pulisce la workspace
    }
  }
}
