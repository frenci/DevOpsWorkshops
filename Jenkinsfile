pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello'
        azureWebAppPublish(azureCredentialsId: '6a42b006-f3c8-41fa-b2f4-7901efeb9a3d', appName: 'app-weu-devops-ms', resourceGroup: 'rg-weu-devops-ms')
      }
    }

  }
}