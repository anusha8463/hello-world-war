pipeline {
    agent none
    stages {
        stage('checkout') {
            steps {	
		    sh 'rm -rf hello-world-war'
		    sh 'git clone https://github.com/anusha8463/hello-world-war/'
            }
        }
	stage('Build') {
            steps {		
	            sh 'mvn clean package'
            }
	}

	stage('deploy') {
            steps {
		echo "Deployed"
	    }
	}
    }
}
