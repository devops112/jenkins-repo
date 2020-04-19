pipeline {
	agent any
	environment {
		docker_home= tool 'my-docker'
		maven_home=tool 'my-maven'
		PATH="$docker_home/bin:maven_home/bin:$PATH"
	}
	stages
	{
	stage('Build') {
		steps
		{
			echo "Build"
			sh 'maven --version'
			sh 'docker version'
			echo "all commands executed"
			
		}
		
	}
	stage('Test') {
		steps{echo "Test"}
		
	}
	stage('INtegration Test')
	{
		steps{echo "Integration Test"}
		
	}
	}
	
	
	post{

		success{
			echo "all the commads are executed without any issues"
		}
	}

}
