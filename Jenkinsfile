pipeline{
     agent any
     tools{
        maven 'Maven'
       // jdk 'jdk'
    }
     stages{
      
          stage ("clone code"){
               steps{
               git url :'https://github.com/shraddha890/MavenProject.git'
               }
          }
     
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
            scp MavenProject/target/webapp
           //withMaven(maven : 'Maven'){
           //sh 'mvn deploy'
     }
      }
       } 
       
       
       }
     }
