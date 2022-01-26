
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...',
                sh './gradlew build --no-daemon',
                archiveArifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
        
        stage('DeployApp') {
            when {
                branch 'master'
            }
            steps {
               execCommand: 'sudo dist/trainSchedule.zip -d /opt/train-schedule && sudo systemctl start train-schedule'
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
