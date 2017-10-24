pipeline {
  agent any
  stages {
    stage('Pre Build') {
      steps {
        parallel(
          "Pre Build": {
            echo 'Building'
            
          },
          "Build": {
            sh '''cd example
mvn install'''
            
          }
        )
      }
    }
  }
}