pipeline {
    agent { docker { image 'node:16.17.1-alpine' } }
    stages {
        stage('Cloning Git') { 
            steps { 
                checkout scm
            }
        } 
        stage('build') {
            steps {
                sh 'node --version'
            }
        }
    }
}