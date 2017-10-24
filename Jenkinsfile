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
            bat 'cd example'
            bat 'mvn install'
            
          }
        )
      }
    }
  }
}