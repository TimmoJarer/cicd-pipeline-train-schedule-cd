pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }        
        stage('Test'){
         when {
              branch 'master'
         }

         steps {
            echo 'Testing...'
            sh 'ls /var/lib/jenkins/jobs/train-schedule/branches/master/builds/17/archive/dist/trainSchedule.zip'
         }
    }
}
}

/*
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
*/
