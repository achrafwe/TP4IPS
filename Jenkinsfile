pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        // echo 'upgrading pip3' chefyuzcvc
        // sh 'pip3 install --upgrade pip'
        echo 'build'
        sh 'pip3 install -r requirements.txt'
      }
    }
    stage('test') {

      steps {
        echo 'test'
        sh 'python3 -m xmlrunner -o test-reports'
      }
      post {
        always {
          junit 'test-reports/*.xml'
        }
      }
    }
  }
}
