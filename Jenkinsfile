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
        echo 'Seccion de Test'
        emailext(subject: 'Prueba de Test', body: 'Se creo un paso para hacer test de funcionamiento a la aplicación', to: 'vhgc.mx@gmail.com', from: 'vhgc.mx@gmail.com')
      }
    }

  }
}