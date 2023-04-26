pipeline { 
    environment { 
        registry = "abhinavprakash1992/Devops" 
        registryCredential = 'dockerhub_id' 
        dockerImage = '' 
    }
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
                    dockerImage = docker.build registry + ":latest" 
                }
            } 
        }     
    }
}