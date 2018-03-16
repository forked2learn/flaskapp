pipeline {
  agent none

  stages {
    stage ("Lint Code") {
      agent { docker 'pylint' }
      steps {
        sh 'pylint --disable=W1202 --output-format=parseable --reports=no module > pylint.log || echo "pylint exited with $?"'
        sh 'cat render/pylint.log'
      }
    }
  }
}
