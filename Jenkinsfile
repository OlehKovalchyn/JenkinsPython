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
      sh 'python -m my_compile ./sources/add2vals.py ./sources/calc.py' 
      }
    }
  }
}
