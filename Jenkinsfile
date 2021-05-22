pipeline {
    agent any
	
	tools {
	      maven 'maven'
		  }

    stages {
        stage('Git checkout') {
            steps {
                echo 'git checkout running'
            }
        } 
        stage('Build Application'){
            steps {
                sh 'mvn clean install'
            }
        }
		 
    }
}
