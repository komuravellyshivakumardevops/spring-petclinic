pipeline {
    agent any 

    stages {
        stage('downloading code') {
            steps {
                git branch: 'main ', url: 'https://github.com/komuravellyshivakumardevops/spring-petclinic.git'
            }
        }
        stage('Building code') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Archiving Artifacts') {
            steps {
                archive 'target/*.jar'
            }
        }    
        stage(' junit test results'){
            steps {
                junit 'target/surefire-reports/*.xml'
            }
         }    
        }
} 
