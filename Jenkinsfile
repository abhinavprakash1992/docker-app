pipeline {
    agent none
    stages {
         stage('Initilize'){
            steps{
                script{
                    def dockerHome = tool 'myDocker'
                env.PATH = "${dockerHome}/bin:${env.PATH}"
                }
            }
        }
        stage('Test') {
         agent { dockerfile true }
            steps {
                sh 'node --version'
                sh 'svn --version'
            }
        }
    }
}