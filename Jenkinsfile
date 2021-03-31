pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "New Try"'
        withSonarQubeEnv(installationName: 'Sonarcube', credentialsId: 'id') {
          waitForQualityGate(abortPipeline: true, credentialsId: 'id')
        }

      }
    }

  }
}
