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
    OWNER = 'jenkins'
  }
}