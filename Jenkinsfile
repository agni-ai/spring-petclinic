pipeline {
  agent any
  stages {
    stage('static analysis') {
      steps {
        withSonarQubeEnv(installationName: 'snq') {
          sh './mvnw clean verify sonar:sonar'
        }
      }
    }

    stage('build') {
      steps {
        sh './mvnw package'
      }
    }

  }
}