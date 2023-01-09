node {
  stage('SCM') {
    checkout scm
  }
 
    stage("SonarQube analysis") {
          script {
              def sonarScanner = tool name: 'SonarQube', type: 'hudson.plugins.sonar.SonarRunnerInstallation'
              bat "${sonarScanner}/bin/sonar-scanner -e -Dsonar.host.url=http://3.8.181.251:9000/"
            }
      }
}
