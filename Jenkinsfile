pipeline {
agent any

stages {
    stage('Open Maintenance Window') {
      steps {
        script {
          MAINTENANCE_ID = sh ( 
            script: './open-window.sh',
            returnStdout: true
          ).trim()
          echo MAINTENANCE_ID
        }
      }
    }
}
}