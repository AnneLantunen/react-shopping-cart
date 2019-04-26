pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:8-alpine'
    }

  }
  stages {
    stage('Install') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh '#npm run test'
      }
    }
    stage('Create docker image') {
      steps {
        sh 'sudo docker build -t demo .'
      }
    }
  }
}