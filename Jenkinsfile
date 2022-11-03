pipeline {
    agent any

    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE = 'sqlite'
    }

    stages {
        stage('Build') {
            steps {
                sh 'printenv'
            }
        }
    }

    post {
        success {
            mail to: 'jhseng@126.com',
                subject: "Success Pipeline: ${currentBuild.fullDisplayName}",
                body: "Build success, ${env.BUILD_URL}"
        }
        failure {
            mail to: 'jhseng@126.com',
                subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
                body: "Something is wrong with ${env.BUILD_URL}"
        }
    }
}
