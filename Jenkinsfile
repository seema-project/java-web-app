pipeline {
    agent any
    
    stages {
        stage('checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/seema-project/java-web-app.git'
            }
        }
        stage('build code') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }
        }
        stage('Deployment'){
			steps{
				deploy adapters: [ tomcat9(url: 'http://54.172.160.13:8080/', credentialsId: 'tomcatCred')], war:'target/*.war'
			}
		}
    }
}