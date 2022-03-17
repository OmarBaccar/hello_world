node {
        stage('SCM') {
	    git credentialsId: 'JENKINS_TOKEN', url: 'https://github.com/OmarBaccar/hello_world.git', branch: 'master'            
        }
        stage('SonarQube Analysis') {

          def scannerHome = tool 'Sonar Scanner';
     	  withSonarQubeEnv('SonarQube') {
            sh "${scannerHome}/bin/sonar-scanner Dsonar.projectKey=hello-python   -Dsonar.sources=.   -Dsonar.host.url=http://20.111.33.243:9000   -Dsonar.login=732963b41eeba56e03614b41946f73397442354a -X"
             }
       } 
        stage('DEPLOY') {
                echo 'deploying app'
        }
    }
