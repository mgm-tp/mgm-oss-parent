pipeline {
    agent any
    tools {
        maven 'Maven 3'
        jdk 'OpenJDK 11'
    }
    stages {
    
        stage ('Build') {
            steps {
                sh 'mvn clean install' 
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
        }
    }
}