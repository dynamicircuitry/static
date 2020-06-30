pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				withAWS(credentials:'aws-static') {
					s3Upload(includePathPattern:'**/*', excludePathPattern;'**/*.md' bucket:"jenkins-static-dyn001", path:'/') 
				}
			}
		}
	}
}
