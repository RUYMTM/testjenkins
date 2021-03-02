pipeline {
    agent any
    tools {
        
        maven "M3"
    }
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/RUYMTM/testjenkins.git'
                bat "mvn clean package"
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
            
        }
    }
}
