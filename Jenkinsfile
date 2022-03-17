node {
        stage('SCM') {
	    git credentialsId: 'JENKINS_TOKEN', url: 'https://github.com/OmarBaccar/hello_world.git', branch: 'master'            
        }
        stage('SonarQube Analysis') {

          def scannerHome = tool 'SonarScanner';
     	  withSonarQubeEnv('SonarQube') {
            sh "${scannerHome}/bin/sonar-scanner -Dsonar.login=732963b41eeba56e03614b41946f73397442354a"
             }
            sh echo "${scannerHome}"
       } 
        stage('DEPLOY') {
                echo 'deploying app'
        }
    }
