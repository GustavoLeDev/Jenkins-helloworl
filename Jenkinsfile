node {
  stage('SCM') {
    checkout scm
  }
  stage('Cloning the project') {
    git 'https://github.com/GustavoLeDev/Jenkins-helloworl.git'
  }
   stage('SonarQube Analysis') {
    def scannerHome = tool 'Sonarqube';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/windows-x86-64/SonarService.bat"
    }
  }
}
