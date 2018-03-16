pipeline {
  agent none

  stages {
    stage ("Lint Code") {
      agent { docker 'pylint' }
      steps {
        sh 'pylint --disable=W1202 --output-format=parseable --reports=no src > pylint.log || echo "pylint exited with $?"'
        sh 'cat pylint.log'
        warnings canComputeNew: false, canResolveRelativePaths: false, categoriesPattern: '', consoleParsers: [[parserName: 'PyLint']], defaultEncoding: '', excludePattern: '', healthy: '', includePattern: '', messagesPattern: '', unHealthy: ''
      }
    }
  }
}
