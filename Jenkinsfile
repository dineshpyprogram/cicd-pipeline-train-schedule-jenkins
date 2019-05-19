pipeline {
  agent any
  steps {
    stages {
      stage ('Build') {
        echo 'running build automation'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
        }
        }
        }
        }
      
