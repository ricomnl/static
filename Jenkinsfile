pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			dir('~/Documents/static') {
				pwd();
				withAWS(region:'us-east-2', credentials:'aws-static') {
					def identity = awsIdentity();
					s3Upload(bucket:'udacity-jenkins-project', workingDir:'dist', includePathPattern:'**/*');
				}
			};
		}
	}
}