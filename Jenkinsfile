pipeline {
  agent {
    docker {
      image 'bryandollery/terraform-packer-aws-alpine'
      args '''-v jenkins_password:/output
-v $PWD:/work
-w /work'''
    }

  }
  stages {
    stage('Checkout') {
      steps {
        sh 'ls'
      }
    }

  }
  environment {
    AWS_PROFILE = 'kh-labs'
    OWNER = 'jenkins'
    AWS_ACCESS_KEY_ID = 'wibble'
    AWS_SECRET_ACCESS_KEY = 'wobble'
  }
}