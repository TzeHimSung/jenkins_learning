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
    stages {
        stage('Test') {
            steps {
                sh 'echo "Fail!"; exit 1'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the stage of the Pipeline has changed'
            echo 'For example, if the Pipelinewas previously failing but is now successful'
        }
    }
}
