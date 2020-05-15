pipeline {

	agent any
	
	stages {
		stage('Tar files') {
			steps {
				sh "tar -czvf ruby_deploy.tar.gz web.rb Dockerfile"
			}
		}
		stage('Publish') { 
			steps { 
				archiveArtifacts 'ruby_deploy.tar.gz'
			}
		}
	}
}