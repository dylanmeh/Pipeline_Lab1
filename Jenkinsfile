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
             emailext (
               subject: "STARTED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
               body: '''<p>STARTED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]':</p> <p>Check console output at &QUOT;<a href='${env.BUILD_URL}'>${env.JOB_NAME} [${env.BUILD_NUMBER}]</a>&QUOT;</p>''',
               to: 'ted.fenn@concanon.com, dylan.mehmedovic@concanon.com'
    )
})
        }       
     }
   }
} 
