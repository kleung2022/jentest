pipeline {
  agent {
    docker {
      image 'python:3.8.10'
      label 'controller'
    }
  }
  stages {
    stage('build') {
      steps {
        sh 'pip install flask'
      }
    }
    stage('test') {
      steps {
        sh 'python src/flask/hello.py'
      }
    }
  }
}
