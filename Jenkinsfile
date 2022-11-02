pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo "Hello Jenkins"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}
