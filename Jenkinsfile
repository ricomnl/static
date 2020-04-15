pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				withAWS(region:'us-east-2', credentials:'aws-static') {
					s3Upload(file:'~/Documents/static/index.html', bucket:'udacity-jenkins-project');
				}
			}
		}
	}
}