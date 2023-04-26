pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                 checkout scm
            }
       
        }
        stage('Build') {
            steps {
                app = docker.build('abhinavprakash1992/Devops')
            }
        }
        stage('Test') {
            steps {
              echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
              docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials'){
              app.push("${env.BUILD_NUMBER}")
              app.push("latest")
            }
        }
        }
    }
}