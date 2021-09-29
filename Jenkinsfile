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
             body: '''STARTED: Job '{$env.JOB_NAME} [{$env.BUILD_NUMBER}]': Check console output at ${env.BUILD_NUMBER}/{$env.JOB_NAME}/{$env.BUILD_NUMBER}''',
            to: 'dylan.mehmedovic@concanon.com'
          )
        }       
     }
   }
} 
