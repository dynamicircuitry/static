pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				withAWS(credentials:'aws-static') {
					s3Upload(bucket:"jenkins-static-dyn0001", path:'', includePathPattern:'**/*', excludePathPattern:'**/*.md,**/Jenkinsfile') 
				}
			}
		}
	}
}
