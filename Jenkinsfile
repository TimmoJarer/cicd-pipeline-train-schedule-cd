pipeline {
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
