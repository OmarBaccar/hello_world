pipeline {
    agent any
    stages { 
	stage('SCM') {
	    git url: 'https://github.com/OmarBaccar/hello_world.git', branch: 'master'            
        }
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
