pipeline {
    agent any
    tools {
        git url: 'https://github.com/RUYMTM/testjenkins.git'
        maven "M3"
    }
    stages {
        stage('Build') {
            steps {
                bat "mvn -B -DskipTests clean package"
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
