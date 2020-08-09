pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile'
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
  environment {
    VAR1 = 'wibble'
  }
}