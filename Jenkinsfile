pipeline {

	agent any
	
	tools {
		go {'go-1.14'}
	}
	
	environment {
		XDG_CACHE_HOME = '/tmp/.cache'
		CGO_ENABLED='0'
	}
	
	stages {
		stage('Our test') {
			steps {
				sh 'go version'
			}
		}
		stage('Test') { 
			steps {
				sh 'go test'
			}
		}
		stage('Build') { 
			steps {
				sh 'go build -o GoServerWithTests'
			}
		}
		stage('Publish') { 
			steps { 
				archiveArtifacts 'GoServerWithTests'
			}
		}
	}
}