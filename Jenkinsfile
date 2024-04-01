pipeline{
    agent any
    stages{
        stage ('checkout code') {
            steps {
                git branch: 'main', url:'https://github.com/seema-project/java-web-app.git'
            }
            
        }
        stage ('build code') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }
        }
        stage ('deploy to tomcat') {
            steps {
                deploy adapters:[tomcat9(url:'http://34.201.252.109:8080/', credentialsId: 'tomcatcred')], war:'**/*.war'
            }
        }
        
     }    
 }
    