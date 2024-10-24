pipeline {
    agent any
    stages {
        stage('No-op') {
            steps {
                sh 'exit 1'  // Cela provoquera un échec
            }
        }
    }
    post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
        success {
            echo 'I succeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        changed {
            echo 'Things were different before...'
        }
    }
}