pipeline {
	agent {
		docker {
			image 'node:6-alpine'
		}
	}
	environnements {
		CI = 'true'
	}
	stages {
		stage('Build') {
			steps {
				sh 'npm install'
			}
		}
		stage('Test') {
			steps { 
				sh './jenkins/scripts/test.sh'
			}
		}
	}
}
