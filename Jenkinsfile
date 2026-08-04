pipeline {
agent any
stages {
stage('Compile') {
steps {
	echo "Compiling.."
}
}
stage('Test') {
steps {
	echo "Running Tests..."
}
}
stage('Approval') {
steps {
	input message: "All tests passed. Continue deployment?", ok: "Approve"
}
}
stage('Deploy') {
steps {
	echo "Application Deployed Successfully."
}
}
}
post {
	success {
	echo "Pipeline Completed."
}
}
}
