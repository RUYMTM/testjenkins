node('docker') {
    checkout scm
    stage('Build') {
        docker.image('maven:3.6.3').inside {
            bat 'mvn --version'
        }
    }
}
