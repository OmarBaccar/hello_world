node {
        stage('SCM') {
	    git credentialsId: 'JENKINS_TOKEN', url: 'https://github.com/OmarBaccar/hello_world.git', branch: 'master'            
        }
        stage('SonarQube Analysis') {

          def scannerHome = tool 'SonarScanner';
     	  withSonarQubeEnv('SonarQube') {
            sh "${scannerHome}/bin/sonar-scanner"
             }
            sh echo "${scannerHome}"
       } 
        stage('DEPLOY') {
                echo 'deploying app'
        }
    }
