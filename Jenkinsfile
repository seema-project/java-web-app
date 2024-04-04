pipeline{
    agent {
        node {
            label 'slave-level-1'
        }
    }
    stages {
        stage ('checkout code'){
            steps {
                git branch: 'main', url: 'https://github.com/seema-project/java-web-app.git'
            }
        }
        stage ('build code'){
            steps{
                sh '/opt/maven/bin/mvn clean package'
            }
        }

    
    }
}