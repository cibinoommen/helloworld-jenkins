pipeline {
agent { docker 'gradle:4.5-jdk8-alpine' }
stages{
	stage('Build') {
		steps {
		 	sh 'gradle clean build'
		 	junit 'build/test-results/**/TEST-*.xml'
		}
	}
	
	stage('Deploy to staging') {
		steps {
			echo "Deploying to staging"
		}
	}
	
	stage ('Deploy to Production') {
		steps {
			echo "deploying to production"
		}
	}
}
}