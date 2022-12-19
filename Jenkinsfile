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
        DOCKERHUB_USER = 'mayowaoluwasina@gmail.com'
        DOCKERHUB_PASSWORD = 'mayor@360'
      }
      steps {
        sh 'docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASSWORD'
      }
    }

  }
}