pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                
                  sh 'mvn -Dmaven.test.failure.ignore=true install'

            }
        }
        
        stage('Dependency Check') {
            
            steps {
                 dependencyCheckAnalyzer datadir: 'data', 
                     true, hintsFile: '', includeCsvReports: false, includeHtmlReports: false, includeJsonReports: false, outdir: '', scanpath: '', skipOnScmChange: false, skipOnUpstreamChange: false, suppressionFile: '', zipExtensions: ''

                 dependencyCheckPublisher canComputeNew: false, defaultEncoding: '', healthy: '', pattern: '', unHealthy: ''
    
                 archiveArtifacts allowEmptyArchive: true, artifacts: '**/dependency-check-report.*', onlyIfSuccessful: true
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
