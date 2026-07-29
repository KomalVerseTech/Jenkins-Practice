pipeline {
	agent any 
	stages {
		stage('checkout') {
			steps {
				echo 'Downloading source code '
			}
		}
		stage('Build'){
			steps {
				sh 'echo "Build started"'
				sh 'date'
				sh 'pwd'
				sh 'ls -la'
			}
		}
		stage('Test') {
			steps {
				echo 'Testing applicationn'
			}
		}
	}
}
