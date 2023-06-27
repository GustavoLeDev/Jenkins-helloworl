node {
  stage('SCM') {
    checkout scm
  }
  stage('Cloning the project') {
    git 'https://github.com/GustavoLeDev/Jenkins-helloworl.git'
  stage('SonarQube Analysis') {
    def scanner = tool 'sonarqube';
    withSonarQubeEnv('sonarqube') {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=Projet_Test -Dsonar.projectName='Projet_Test'"
    }
  }
}
