pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "New Try 2"'
        withSonarQubeEnv(installationName: 'Sonarcube', credentialsId: 'id') {
          waitForQualityGate(abortPipeline: true, credentialsId: 'id')
        }

      }
    }

  }
}