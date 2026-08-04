pipeline {
	agent any 
	stages {
		stage('Clean') {
			steps {
				sh 'mvn clean'
			}
		}
		stage('Build'){
			steps {
				sh 'mvn compile'
			}
		}
		stage('Test') {
			steps {
				sh 'mvn test'
			}
		}
		stage('Package') {
			steps {
				sh 'mvn package'
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
			echo 'Pipeline execution completed'
}
		success {
			echo 'Build, Test and Package Successful'
		}
		failure {
			echo 'Pipelinne Failed - check console output'
		}
	}
}
