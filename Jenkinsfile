/* groovylint-disable-next-line CompileStatic */
pipeline {
      agent none

      environment {
                  dotnet = 'C:\\Program Files\\dotnet\\dotnet.exe'
      }

      stages {
            stage('Build') {
                  steps {
                        bat 'dotnet build JenkinsIntegration\\jenkinsIntegration.sln --configuration Release'
                  }
            }
            stage('Test') {
                  steps {
                        bat 'dotnet test JenkinsIntegration\\JenkinsIntegration.Tests\\JenkinsIntegration.Tests.csproj --logger:trx'
                  }
            }
            stage('Publish') {
                  steps {
                        bat 'dotnet publish JenkinsIntegration\\jenkinsIntegration\\jenkinsIntegration.csproj'
                  }
            }
      }
}
