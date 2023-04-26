node {
    stage('Initialize'){
        def dockerHome = tool 'myDocker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
    }
    checkout scm
     
    def customImage = docker.build("my-image")

    customImage.inside {
        sh 'make test'
    }
}
