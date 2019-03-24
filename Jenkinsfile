pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'make check'
            }
        }
    }
    post {

        failure {
            mail to: jesuisdelaplanetemars3@example.com, subject: 'The Pipeline failed'
        }
    }
}
