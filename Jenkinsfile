pipeline {
    agent any
    stages {
        stage('SCM') {
	    git 'https://github.com/OmarBaccar/hello_world.git', branch: 'master'            
        }
        
        stage('DEPLOY') {
                echo 'deploying app'
        }
    }
}
