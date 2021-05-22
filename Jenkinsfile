pipeline {
    agent any
	
	tools {
	      maven 'maven'
		  }

    stages {
        stage('Git checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/natiy/mule-maven-deployment-demo.git']]])
            }
        } 
        stage('Build Application'){
            steps {
                sh 'mvn clean install'
            }
        }
		 
    }
}
