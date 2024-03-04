pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        bat 'py -3 --version'
      }
    }
    stage('hello') {
      steps {
        sh 'py -3 hello.py'
      }
    }
  }
}
