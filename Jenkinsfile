pipeline {
    agent { docker { image 'golang:1.22.0-alpine3.19' } }

    stages {
        stage('Build') {
            steps {
                script {
                    def goHome = tool name: 'Go', type: 'go'
                    env.GOPATH = "${env.WORKSPACE}/go"
                    env.PATH = "${goHome}/bin:${env.PATH}"
                }
                sh 'go build -o hello'
            }
        }
        stage('Run') {
            steps {
                sh './hello'
            }
        }
    }

    post {
        success {
            echo 'Build successful'
        }
        failure {
            echo 'Build failed'
        }
    }
}
