node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'sonar_qube';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
      sonar-scanner \
        -Dsonar.projectKey=iti_lab \
        -Dsonar.sources=python.py \
        -Dsonar.login=sqp_0fc48057d69314661c45895c6a07c4dee3cd2e07
    }
  }
}
