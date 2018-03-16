pipeline {
  agent none

  stages {
    stage ("Lint Code") {
      agent { docker 'pylint' }
      steps {
        sh 'python --version'
        sh 'pwd'
        sh 'ls'
      }
    }
  }
}
