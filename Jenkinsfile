pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        git(url: 'https://github.com/AbrahamMayowa/jen-test.git', branch: 'main')
      }
    }

    stage('docker login') {
      agent any
      environment {
        DOCKERHUB_USER = 'mayorfullstack'
        DOCKERHUB_PASSWORD = 'mayor@360'
      }
      steps {
        sh 'sudo docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASSWORD'
      }
    }

    stage('Push docker image') {
      steps {
        sh 'sudo docker push mayorfullstack/jenkin-node:latest'
      }
    }

  }
}