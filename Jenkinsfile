pipeline {
    agent any

    stages {
        stage('Git checkout') {
            steps {
                echo 'git checkout running'
            }
        } 
        stage('Build Application'){
            steps {
                sh 'mvn --version'
            }
        }
		 
    }
}
