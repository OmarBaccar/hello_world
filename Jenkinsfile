pipeline {
    agent any
    stages {
        stage('SCM') {
            steps{
	    git 'https://github.com/OmarBaccar/hello_world.git', branch: 'master'            
        }
        }
        
        stage('DEPLOY') {
            steps{
                echo 'deploying app'
        }
	}
    }
}
