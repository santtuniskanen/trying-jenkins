pipeline {
    agent any

    tools {
        go '1.22.0'
    }

    stages {
        stage('Build') {
            steps {
                sh 'go build -o hello'
                sh 'echo "Hello, world!"'
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
