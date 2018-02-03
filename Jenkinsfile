pipeline {
  agent {
      docker {
          image 'ubuntu:latest'
      }
  }
  stages {
    stage('test') {
      steps {
        sh "docker -v"
        sh "docker pull ubuntu"
      }
    }
  }
}
