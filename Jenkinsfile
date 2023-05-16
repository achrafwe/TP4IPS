pipeline {
  agent { 
    docker { 
      image 'python:3.7.2'
    }
  }
  stages {
    stage('build') {
      steps {
        echo 'upgrading pip3'
        sh 'pip3 install --upgrade pip'
        echo 'build'
        sh 'pip3 install -r requirements.txt'
      }
    }
    stage('test') {

      steps {
        echo 'test'
        sh 'python test.py'
      }
      post {
        always {
          junit 'test-reports/*.xml'
        }
      }
    }
  }
}
