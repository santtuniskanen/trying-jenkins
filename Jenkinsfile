pipeline {
    agent { docker { image 'golang:1.22.0-alpine3.19' } }
    stages {
        stage('build') {
            steps {
	    	sh 'echo "Hello, World!"'
                sh 'go build'
		sh './trying-jenkins'
            }
        }
    }
}
