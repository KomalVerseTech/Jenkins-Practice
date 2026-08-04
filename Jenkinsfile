pipeline {
	agent any
	parameters {
		choice(
			name: 'ENV',
			choices: [
				'DEV',
				'QA',
				'PROD'
				],
			description: 'Select Environment'
			)
	}
	stages {
		stage('Build') {
			steps {
				echo "Building..."
			}
		}
		stage('Deploy') {
			when {
				expression {
					return params.ENV == "PROD"
				}
			}
			steps {
				echo "Deploying to Production"
			}
		}
	}
}
