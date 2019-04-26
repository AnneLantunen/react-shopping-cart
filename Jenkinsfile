pipeline {
  agent any
  stages {
    stage('Docker image') {
      steps {
        sh 'docker run build -t demo .'
      }
    }
    stage('Run docker') {
      steps {
        sh 'docker run -t -p 3000:8001 demo'
      }
    }
  }
}