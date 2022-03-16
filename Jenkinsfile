pipeline {
    agent any
    stages {
        stage('BUILD') {
            steps {
                echo 'building app '
            }
        }
        stage('TEST') {
            steps {
                echo 'Testing app'
            }
        }
	stage('SonarQube Analysis') {
         steps {      
        def scannerHome = tool 'SonarScanner';
           withSonarQubeEnv() {
              sh "${scannerHome}/bin/sonar-scanner"
        }
        }
         }
        stage('DEPLOY') {
            steps {
                echo 'deploying app'
            }
        }
    }
}
