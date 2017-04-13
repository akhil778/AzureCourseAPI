pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''bat 'nuget restore AzureCourseAPI.sln'
bat "\"${tool 'MSBuild'}\" AzureCourseAPI.sln /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"'''
      }
    }
  }
}