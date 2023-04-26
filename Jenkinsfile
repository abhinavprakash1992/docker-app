pipeline { 
    agent any 
    stages {
        stage('Initilize'){
            steps{
                script{
                    def dockerHome = tool 'myDocker'
                    env.PATH = "${dockerHome}/bin:${env.PATH}"
                }
            }
        }
        stage('Cloning Git') { 
            steps { 
                checkout scm
            }
        } 
        stage('Building image') { 
            steps { 
                script { 
                    dockerImage = docker.build('latest') 
                }
            } 
        }     
    }
}