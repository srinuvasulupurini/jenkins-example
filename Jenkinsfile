pipeline {
	agent {  label 'linux-node1' }
	stages {
		stage('---clean----'){
			tools {
				maven 'maven-3.8.6'
			}
			steps {
				sh 'mvn --version'
				sh "mvn clean"
			}
		}
		stage('---test---') {
			tools {
				maven 'maven-3.8.4'
			}
			steps {
				sh 'mvn --version'
				sh "mvn test"
			}
		}
		stage('---package---'){
			tools {
				maven 'maven-3.8.4'
			}
			
			steps {
				sh 'mvn --version'
				sh "mvn package"
			}
		}
	}
	post {
		success {
			echo 'job was built successfully'
		}
		failure {
			echo 'job was not build..it was failed'
		}
	}
}
