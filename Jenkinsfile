pipeline {
    agent { docker { 
    	image 'golang:1.22.0-alpine3.19' 
	args '-v $HOME/.cache:/go/.cache' 
	} 
    }
    stages {
        stage('build') {
            steps {
	    	sh 'echo "Hello, World!"'
                sh 'go build -o hello'
		sh './hello'
            }
        }
    }
}
