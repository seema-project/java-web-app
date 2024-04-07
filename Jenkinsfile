node('any') {    
    stage('checkout code') {
        git branch: 'main', url: 'https://github.com/seema-project/java-web-app.git'
    }
    stage('build code') {
        sh '/opt/maven/bin/mvn clean package'
    }
    stage('Deployment'){
		deploy adapters: [ tomcat9(url: 'http://54.172.160.13:8080/', credentialsId: 'tomcatCred')], war:'**/*.war'
	}
}