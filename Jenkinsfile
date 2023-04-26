node {
    stage('Clone repository') {
        checkout scm
    }
    stage('Build image') {
        dockerImage = docker.build('abhinavprakash1992/Devops')
    }
    stage('Push image') {
        dockerImage.push("latest")
    }
}