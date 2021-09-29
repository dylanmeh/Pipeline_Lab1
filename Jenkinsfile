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
            body: '''<p>STARTED: Job '"$JOB_NAME" ["$BUILD_NUMBER"]':</p> <p>Check console output at &QUOT;<a href='"$BUILD_URL"'>"$JOB_NAME" ["$BUILD_NUMBER"]</a>&QUOT;</p>''',
            to: 'dylan.mehmedovic@concanon.com'
          )
        }       
     }
   }
} 
