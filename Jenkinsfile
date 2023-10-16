pipeline {
    agent none
    stages {
        stage('checkout') {
		agent {
	    		label 'slave1'
    		}
            steps {	
		    sh 'rm -rf hello-world-war'
		    sh 'git clone https://github.com/anusha8463/hello-world-war/'
            }
        }
	stage('Build') {
		agent {
	    		label 'slave2'
    		}
            steps {		
	            sh 'mvn clean package'
            }
	}

	stage('deploy') {
            steps {
		    echo "Deployed"
		//sh 'sudo cp /var/lib/jenkins/workspace/Multibranch_pipeline_develop/target/hello-world-war-2.0.0.war /var/lib/tomcat9/webapps'
	    }
	}
    }
}
