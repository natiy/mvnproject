
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
        stage('Maven Testing') {
          steps {
            sh 'mvn test'
            echo 'maven testing going on'
          }
        }

      stage('s3Upload artifact'){
        steps {
          s3Upload consoleLogLevel: 'INFO', dontSetBuildResultOnFailure: false, dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 'sri-devops2223', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: false, noUploadOnFailure: false, selectedRegion: 'us-east-1', showDirectlyInBrowser: false, sourceFile: 'Demo-java-project/target/*.war', storageClass: 'STANDARD', uploadFromSlave: false, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 's3_jenkins', userMetadata: []

        }
      }

    }
}
