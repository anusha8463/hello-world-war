pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {	

                sh 'git clone https://github.com/anusha8463/hello-world-war/'
            }
        }
	stage('Build') {
            steps {		

                sh 'mvn clean package'
            }
        }    
    }
}
