pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                
                 sh '/usr/share/maven 3.0.5 clean install'

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
