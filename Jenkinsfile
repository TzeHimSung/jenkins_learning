pipeline {
    agent {
        docker {
            image 'node:7-alpine'
            args '--privileged'
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}
