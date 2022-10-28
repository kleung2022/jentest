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
        sh 'pip install --target /home/jenkins/agent/workspace flask'
        sh 'python ./src/flask/hello.py &'
      }
    }
    stage('test') {
      steps {
        echo "${env.NODE_NAME}"
      }
    }
  }
}
