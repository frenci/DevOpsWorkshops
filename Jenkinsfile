pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello'
        git(credentialsId: '	github', url: 'https://github.com/mskuratowski/DevOpsWorkshops.git', branch: 'master')
        dotnetRestore()
        dotnetBuild(configuration: 'Release')
        dotnetPublish(configuration: 'Release')
      }
    }

  }
}