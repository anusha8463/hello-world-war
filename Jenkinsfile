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
	stage('Tomcat Installation') {
            steps {
		    sh 'sh tomscript.sh'
		    echo "Tomcat installed in slave1"
            }
        }

	stage('deploy') {
            steps {
		    
		sh 'sudo cp /home/ubuntu/workspace/tomcat_pipeline/target/hello-world-war-2.0.0.war /var/lib/tomcat9/webapps'
	    }
	}
    }
}
