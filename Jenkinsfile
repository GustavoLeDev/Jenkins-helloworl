node {
  stage('SCM') {
    checkout scm
  }
  stage('Cloning the project') {
    git 'https://github.com/GustavoLeDev/Jenkins-helloworl.git'
  }
   stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
