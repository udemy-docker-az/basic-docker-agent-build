pipeline {
  agent a
  stages {
    stage('npm version') {
      agent {
        docker {
          image: 'node:latest'
        }
      }
      steps {
        sh "npm -v"
      }
    }
  }
}
