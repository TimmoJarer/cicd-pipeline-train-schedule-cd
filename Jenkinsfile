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
            sh 'unzip /var/lib/jenkins/jobs/train-schedule/branches/master/builds/19/archive/dist/trainSchedule.zip -d /opt/train-schedule'
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
