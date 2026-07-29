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
				sh 'echo "Hello Jenkins" > output.txt'
				sh 'cat output.txt'
			}
		}
		stage('Test') {
			steps {
				echo 'Testing applicationn'
			}
		}
		stage('Archive') {
			steps {
				archiveArtifacts artifacts: 'output.txt'
	}
}
