pipeline {
  agent {
    docker {
      image 'hashicorp/packer'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        sh '''ls
pwd
whoami'''
      }
    }

    stage('build') {
      steps {
        sh 'packer build packer.json'
      }
    }

  }
}