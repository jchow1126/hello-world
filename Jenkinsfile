pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Test Blue Ocean'
          }
        }
        stage('Validate package') {
          steps {
            powershell '& $env:TESTINGSCRIPTDIR\\Validate-Package.ps1'
          }
        }
      }
    }
  }
}