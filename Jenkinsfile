pipeline {
   agent any
   stages {
     stage('Hello World') {
        steps {
          sh 'echo Hello World'
        }
     }   
   stage('Email') {
        steps {
          emailext (
             subject: "STARTED: Job {$env.JOB_NAME} [{$env.BUILD_NUMBER}]",
             body: '''<p>STARTED: Job '{$env.JOB_NAME} [{$env.BUILD_NUMBER}]':</p> <p>Check console output at "<a href=[${env.BUILD_NUMBER}]>{$env.JOB_NAME} [{$env.BUILD_NUMBER}]"</p>''',
            to: 'dylan.mehmedovic@concanon.com'
          )
        }       
     }
   }
} 
