pipeline {
	agent any
	environment {
		docker_home= tool 'mydocker'
		maven_home= tool 'mymaven'
		PATH= "$docker_home/bin:$maven_home/bin:$PATH"
	}
	stages
	{
	stage('Build') {
		steps
		{
			echo "Build"
			echo "PATH = $PATH"
			sh 'mvn --version'
			sh 'sudo su'
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
