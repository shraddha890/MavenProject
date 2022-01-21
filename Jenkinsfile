pipeline{
     agent any
     environment {
     }
     
     
     
     stages{
      
          stage ("clone code"){
               steps{
               git url :''}}
     
      stage ('Build Stage'){
      steps{
           withMaven(maven : 'Maven'){
           sh 'mvn clean package'
     }
      }
       } 
       
       stage ('Test Stage'){
       steps{
           withMaven(maven : 'Maven'){
           sh 'mvn test'
     }
      }
       } 
      
       stage ('Deploy Stage'){
       steps{
           withMaven(maven : 'Maven'){
           sh 'mvn deploy'
     }
      }
       } 
       
       
       }
     }
