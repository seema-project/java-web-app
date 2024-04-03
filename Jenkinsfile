pipeline {
    agent {
        node{
            label 'jenkins-slave-node'
        }
    }
    stages {
        stage ('checkoutcode') {
            steps{
                git branch: 'main' , url: 'https://github.com/seema-project/java-web-app.git'
            }
        }
        stage ('buildcode'){
            steps{
                sh '/opt/maven/bin/mvn clean package'
            }
        }
       

    }
}
    