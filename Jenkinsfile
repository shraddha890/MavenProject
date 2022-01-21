pipeline{ 
     agent any
     
     def tomcatWeb = 'C:\\Program Files\\Apache Software Foundation\\Tomcat9\\webapps'
     def  tomcatBin = 'C:\\Program Files\\Apache Software Foundation\\Tomcat9\\bin'
     def tomcatStatus=''
     tools{
        maven 'Maven'
       // jdk 'jdk'
    }
     stages{
      
          stage ("SCM Checkout"){
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
      
       stage ('Deploy To Tomcat'){
       steps{
            sh "copy target\\MavenWebProject.war \"${tomcatWeb}\\MavenWebProject.war\""
       }
        }
            
           
                    
          
       
       
       
       }
     }
