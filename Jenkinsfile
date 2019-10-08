pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000 -p 5000:5000'
    }

  }
  stages {
    stage('Build') {
      environment {
        CI = 'true'
      }
      steps {
        sh 'npm install'
        sh ' sh \'./jenkins/scripts/test.sh\''
      }
    }
  }
}