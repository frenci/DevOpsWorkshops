pipeline {
  agent any
  stages {
    stage('') {
      steps {
        echo 'Hello'
        git(credentialsId: '	github', url: 'https://github.com/mskuratowski/DevOpsWorkshops.git', branch: 'master')
        dotnetRestore()
        dotnetBuild(configuration: 'Release')
        dotnetPublish(configuration: 'Release')
        azureWebAppPublish(azureCredentialsId: 'azure-devops-connection', appName: 'app-weu-devops-ms', resourceGroup: 'rg-weu-devops-ms')
      }
    }

  }
}