pipeline {
  agent any
  stages {

    stage('build') {
      steps {
        sh './mvnw package'
      }
    }

    stage('deploy') {
      steps {
        ansiblePlaybook(credentialsId: '/home/id_rsa', inventory: '/home/hosts', playbook: '/home/playbook.yml')
      }
    }

  }
}