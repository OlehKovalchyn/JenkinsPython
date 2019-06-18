pipeline {
  agent none
  stages {
    stage('Buld') {
      agent {
        docker{
          image 'python:2-alpine'
        }
      }
      steps{
      sh 'python try1.py' 
      }
    }
  }
}
