node {
  stage('SCM') {
    git 'https://github.com/nikolaypeshev-86/sonarscanner.git'
  }
  stage('SonarQube Analysis') {
          sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=Sonar -Dsonar.host.url=http://bgsovm00017.corp.polygran.de:9000 -Dsonar.login=sqp_f3682128003b51a07e9347843bba5d409b4f8203 -Dsonar.analysis.buildNumber=${BUILD_NUMBER} -Dsonar.analysis.jobName=${JOB_NAME}'
  }
}
