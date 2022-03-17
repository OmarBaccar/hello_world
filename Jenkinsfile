pipeline {
    agent any
    stages {
        stage('SCM') {
            steps{
	    git credentialsId: 'JENKINS_TOKEN', url: 'https://github.com/OmarBaccar/hello_world.git', branch: 'master'            
        }
        }
        stage('SonarQube Analysis') {
        steps{
          script {
   		 def scannerHome = tool 'SonarScanner 2.14';}
     
     	  withSonarQubeEnv('SonarQube') {
            sh "${scannerHome}/bin/sonar-scanner"
    }
  }} 
        stage('DEPLOY') {
            steps{
                echo 'deploying app'
        }
	}
    }
}
