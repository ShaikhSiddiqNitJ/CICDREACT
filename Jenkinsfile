pipeline {
  agent {
    docker {
      image 'node:18'
    }
  }

  stages {
    stage('Install') {
      steps {
        sh 'npm install'
      }
    }

    stage('Build') {
      steps {
        sh 'npm run build'
      }
    }

    stage('Start') {
      steps {
        sh 'nohup npm start &'
      }
    }
  }
}
