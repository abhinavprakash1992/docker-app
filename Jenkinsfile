node {
    stage('Clone repository') {
        checkout scm
    }
    stage('Build image') {
        dockerImage = docker.build('abhinavprakash1992/Devops')
    }
    stage('Push image') {
        withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials'){
        dockerImage.push("latest")
        }
    }
}