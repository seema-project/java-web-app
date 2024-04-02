node {
    
    stage ('checkout code') {
           
         git branch: 'main', url:'https://github.com/seema-project/java-web-app.git'

    }
     stage ('build code') {
           
         sh '/opt/maven/bin/mvn clean package'
    }
        
    stage ('deploy to tomcat') {
           
        deploy adapters:[tomcat9(url:'http://44.201.255.160:8080/', credentialsId: 'tomcatcred')], war:'**/*.war'
     }
        }
        
       
 
    