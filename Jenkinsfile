pipeline {
    agent any 
    stages {
        stage('clean') { 
            steps {
               sh "mvn clean"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test"
            }
        }
        stage('Validate') { 
            steps {
                sh "mvn package"
            }
        }
	stage('Deploy') {
            steps {
                sh "cp web-app.war /opt/tomcat/latest/webapps"
            }
        }
    }
}
