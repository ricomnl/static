pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			withAWS(region:'us-east-2', credentials:'aws-static') {
				def identity = awsIdentity();
				s3Upload(file:'~/Documents/static/index.html', bucket:'udacity-jenkins-project');
			}
		}
	}
}