pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ansariarham221106-ctrl/tomcat-project.git'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Deploy') {
            steps {
                bat 'mvn tomcat7:deploy'
            }
        }
    }
}