pipeline {
  agent {
    docker {
      image 'node:12'
      args '--network dok21_mynet'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'echo "npm install esto se comento"'
          }
        }

        stage('Notificacion') {
          steps {
            slackSend(attachments: 'Attachments', botUser: true, channel: 'notifica-jenkins', message: 'Inicio de Blue Ocean', notifyCommitters: true, teamDomain: 'devopstest-espacio', tokenCredentialId: 'dwu2sLpd9gVAE6CleIrRdPGA', username: 'Test-vhgc', blocks: 'Uno 1')
          }
        }

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