pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello'
        git(credentialsId: '	github', url: 'https://github.com/mskuratowski/DevOpsWorkshops.git', branch: 'master')
        sh 'dotnet build --configuration Release'
        archiveArtifacts 'drop'
      }
    }

  }
}