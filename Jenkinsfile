pipeline {
    agent {
	    label 'slave1'
    }
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
		sh 'sudo cp /var/lib/jenkins/workspace/Multibranch_pipeline_develop/target/hello-world-war-2.0.0.war /var/lib/tomcat9/webapps'
	    }
	}
    }
}
