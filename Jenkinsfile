node (label: 'Linux') {
        stage('SCM') {
	    git url: 'https://github.com/OmarBaccar/hello_world.git', branch: 'master'            
        }
        stage('SonarQube Analysis') {

          echo 'scanning code'
       } 
        stage('DEPLOY') {
                echo 'deploying app'
        }
    }
