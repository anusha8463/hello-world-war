pipeline {
	agent {
	    		label 'slave1'
    	}
    stages {
	stage('Tomcat Installation') {
            steps {	
		    sh tomscript.sh
		    echo "Tomcat installed in slave1"
            }
        }
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
		    
		sh 'sudo cp /var/lib/jenkins/workspace/tomcat_pipeline_master/target/hello-world-war-1.0.0.war /var/lib/tomcat9/webapps'
	    }
	}
    }
}
