node {
    def app
    stage('Initialize'){
        def dockerHome = tool 'myDocker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
    }
    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build('abhinavprakash1992/Devops')
    }
}