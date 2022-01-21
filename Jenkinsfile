pipeline{
     agent any
     
     stages{
     
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
