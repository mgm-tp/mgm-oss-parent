pipeline {
    agent any
    tools {
        maven 'Maven 3'
        jdk 'OpenJDK 11'
    }
    stages {
    
        stage ('Build') {
            steps {
                configFileProvider([
					configFile(fileId: 'mgm-maven-settings', variable: 'MAVEN_SETTINGS_XML')
				]) {
                    sh 'mvn clean install -s $MAVEN_SETTINGS_XML'
                } 
            }
            
        }
    }
}