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
           deploy adapters: [tomcat8(url: 'http://localhost:8080/', 
                              credentialsId: 'manager')], 
                war: 'target/*.war'}
                    
           // scp MavenProject/target/MavenWebProject.war ec2-user@17:32:39.688:
           // scp <src_file> username@IP:<dest_path>
           //withMaven(maven : 'Maven'){
           //sh 'mvn deploy'
     }
      
       
       
       
       }
     }
