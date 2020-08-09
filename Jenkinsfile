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
'''
      }
    }

    stage('build') {
      steps {
        timeout(time: 3, unit: 'MINUTES') {
          sh 'packer build packer.json'
        }

      }
    }

    stage('Test') {
      steps {
        git(url: 'https://github.com/KnowledgeHut-AWS/jenkins', branch: 'master')
      }
    }

    stage('Release') {
      steps {
        echo 'tag ami'
      }
    }

  }
}