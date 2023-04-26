pipeline {
    agent { dockerfile true }
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
            steps {
                sh 'node --version'
                sh 'svn --version'
            }
        }
    }
}