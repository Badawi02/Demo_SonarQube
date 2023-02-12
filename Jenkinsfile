pipeline {
    agent any
    stages {
        stage('SonarQube Analysis') {
            steps {
              script {
                def scannerHome = tool 'sonar_qube';
                withSonarQubeEnv("iti_lab") {
                sh "${scannerHome}/bin/sonar-scanner"
                }
              }
            }
        }
    }
}
