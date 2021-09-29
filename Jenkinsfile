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
           emailext body: '''pipeline was successful.

           Lab 1 complete''', subject: 'Lab1 pipeline', to: 'ted.fenn@concanon.com, dylan.mehmedovic@concanon.com'
        }       
     }
   }
} 
