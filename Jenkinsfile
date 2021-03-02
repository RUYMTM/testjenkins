pipeline {
    agent any
    tools {
        
        maven "M3"
    }
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/RUYMTM/testjenkins.git'
                bat "mvn compile"
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}
