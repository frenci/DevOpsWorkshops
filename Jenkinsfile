pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello'
        git(credentialsId: '	github', url: 'https://github.com/mskuratowski/DevOpsWorkshops.git', branch: 'master')
        dotnetClean(configuration: 'Release')
        dotnetToolRestore()
        dotnetBuild(configuration: 'Release')
        dotnetPublish(configuration: 'Release')
        archiveArtifacts 'drop'
      }
    }

  }
}