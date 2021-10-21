pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Hello'
        git(credentialsId: '71cf3766-34d2-4753-af18-47d34b8d70a6', url: 'https://github.com/mskuratowski/DevOpsWorkshops.git', branch: 'master')
        dotnetRestore()
        dotnetBuild(configuration: 'Release')
        dotnetPublish(configuration: 'Release')
        sh 'echo \'Hello World\''
      }
    }

  }
}