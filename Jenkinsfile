pipeline {
  agent {
    docker {
      image 'node:12'
      args '--network dok_mynet'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Ejecutar') {
      steps {
        sh 'npm run dev'
      }
    }

  }
}