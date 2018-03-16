pipeline {
  agent none

  stages {
    stage ("Lint Code") {
      agent { docker 'python:3' }
      steps {
        python --version
      }
    }
  }
}
