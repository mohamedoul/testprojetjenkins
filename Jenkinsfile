pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                
                  sh 'mvn -Dmaven.test.failure.ignore=true install'

            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
