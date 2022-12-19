pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        git(url: 'https://github.com/AbrahamMayowa/jen-test.git', branch: 'main')
      }
    }

    stage('buid docker image') {
      steps {
        sh 'sudo docker build -f jen-test/Dockerfile -t mayorfullstack/jenkin-node:latest .'
      }
    }

  }
}