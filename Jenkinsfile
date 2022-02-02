/*
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh './gradlew build --no-daemon'
                archiveArifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
         stage('Test'){
         when {
              branch 'master'
         }

         steps {
            echo 'Testing...'
         }
    }
}
}
*/

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}

