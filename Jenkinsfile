pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'cat /var/jenkins_home/secrets/master.key'
            }
        }
    }
}