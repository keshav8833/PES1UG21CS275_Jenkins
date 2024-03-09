pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS275-1'
        sh 'g++ hello.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        ech 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
