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
         withCredentials([usernamePassword(credentialsId: 'admin', usernameVariable: 'USERNAME', passwordVariable: 'USERPASS')]){ 
            
            echo 'Testing...'
            sh 'unzip /var/lib/jenkins/jobs/train-schedule/branches/master/builds/25/archive/dist/trainSchedule.zip -d /tmp/train-schedule'
            sh 'sudo systemctl start trains -u $USERNAME -p $PASSWORD'
            }
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
