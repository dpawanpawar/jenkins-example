pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'py -3 --version'
      }
    }
    stage('hello') {
      steps {
        sh 'python3 hello.py'
      }
    }
  }
}
