pipeline {
  agent none
  stages {
    stage('docker npm version') {
      agent {
          docker { image 'node:latest' }
      }
      steps {
        sh "node -v"
        sh "npm -v"
      }
    }
    stage('docker container script'){
      steps{
        docker.image("node:latest").inside {
          sh 'node -v'
          sh 'npm -v'
        }
      }
    }
  }
}
