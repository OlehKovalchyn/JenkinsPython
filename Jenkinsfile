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
      sh 'python ./sources/calc.py' 
      }
    }
  }
                stage('Test') { 
            agent {
                docker {
                    image 'qnib/pytest' 
                }
            }
            steps {
                sh 'py.test --verbose --junit-xml test-reports/results.xml ./sources/test_calc.py' 
            }
            post {
                always {
                    junit 'test-reports/results.xml' 
                }
            }
}

