pipeline {
	agent any
	parameters {
		booleanParam(
			name: 'DEPLOY',
			defaultValue: true,
			description: 'Deploy Application?'
)
}
stages {
	stage('Build') {
		steps {
			echo "Building Application ..."
}
}
stage('Deploy') {
 when {
	expression {
		return params.DEPLOY
}
}
steps {
	echo "Deploying Application..."
}
}
}
}
