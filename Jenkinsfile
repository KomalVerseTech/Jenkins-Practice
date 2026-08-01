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
				sh 'mvn clean package'
			}
		}
		stage('Verify') {
			steps {
				echo 'ls -l target'
			}
		}
		stage('Archive') {
			steps {
				archiveArtifacts artifacts: 'target/*.jar'
	}
}
	}
	post {
		always {
			echo 'Pipeline Finished'
}
		success {
			echo 'Maven Build Successful'
		}
		failure {
			echo 'Maven Build Failed'
		}
	}
}
