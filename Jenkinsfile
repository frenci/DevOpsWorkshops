pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello'
        azureWebAppPublish(azureCredentialsId: 'azure-devops-connection', appName: 'app-weu-devops-ms', resourceGroup: 'rg-weu-devops-ms')
      }
    }

  }
}