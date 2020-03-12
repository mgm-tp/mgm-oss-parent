pipeline {
    agent {
        label {
                label "Build Slave"
        }
    }
    stages { 
        stage ('Build') {
            steps {
                withMaven(globalMavenSettingsConfig: 'mgm-maven-settings', jdk: 'OpenJDK 11', maven: 'Maven 3')  {
                    sh 'mvn clean install'
                } 
            }
            
        }
    }
}