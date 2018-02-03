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
        script{
          def nodeLatest = docker.pull("node:latest")

          nodeLatest.inside {
            sh 'node -v'
            sh 'npm -v'
          }  
        }
      }
    }
  }
}
