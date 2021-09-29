pipeline {
   agent any
   stages {
     stage('Hello World') {
        steps {
          sh 'echo Hello World'
          echo "STARTED: Job "$env.JOB_NAME" "[$env.BUILD_NUMBER]""
        }
     }   
   }
} 
