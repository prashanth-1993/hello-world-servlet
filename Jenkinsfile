pipeline {
  agent any
    tools {
      maven 'mymaven'
    }
    stages {
          stage('preparation of code checkout'){
               steps {
            
                   git 'https://github.com/prashanth-1993/hello-world-servlet.git'
                }
           }
      
     stage ('building the code') {
       steps {
         sh 'mvn install'
         
       }
     }
      stage ('unit tests'){
        steps {
         junit '**/build/test-reports/*.xml'
        }
      }
   }    
 }
