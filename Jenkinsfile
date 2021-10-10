pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello'
        git(credentialsId: '	github', url: 'https://github.com/mskuratowski/DevOpsWorkshops.git', branch: 'master')
        sh '''dotnet restore
dotnet clean
dotnet build --configuration Release
dotnet publish
'''
      }
    }

  }
}