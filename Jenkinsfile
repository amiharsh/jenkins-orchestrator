pipeline {
agent any

stages {
    stage('Open Maintenance Window') {
      steps {
        script {
          sh '''
          set +x
          chmod a+x open-window.sh
          '''
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