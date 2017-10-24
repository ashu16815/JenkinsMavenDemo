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
'''
            
          },
          "Post Build": {
            echo 'Post Build Step'
            
          }
        )
      }
    }
    stage('Env Provisioning ') {
      steps {
        parallel(
          "Env Provisioning ": {
            echo 'env provisioned '
            
          },
          "Validation ": {
            echo 'validation'
            
          }
        )
      }
    }
    stage('Pre Deploy') {
      steps {
        parallel(
          "Pre Deploy": {
            echo 'pre deploy step executed'
            
          },
          "Deploy": {
            echo 'Deployment Done'
            
          },
          "Post deploy ": {
            echo 'post deployment'
            
          }
        )
      }
    }
    stage('Performance Test') {
      steps {
        parallel(
          "Performance Test": {
            echo 'performace test'
            
          },
          "Functional Test": {
            echo 'Functional test'
            
          },
          "Security Test": {
            echo 'security test'
            
          }
        )
      }
    }
  }
}