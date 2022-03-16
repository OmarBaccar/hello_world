pipeline {
    agent any
    stages {
        stage('SCM') {
	    git 'https://github.com/OmarBaccar/hello_world.git', branch: 'master'            
        }
	stage('SonarQube Analysis') {
           def scannerHome = tool 'SonarScanner';
           withSonarQubeEnv('SonarQube Scanner') {
              sh "${scannerHome}/bin/sonar-scanner"
        }
         }
        stage('DEPLOY') {
                echo 'deploying app'
        }
    }
}
