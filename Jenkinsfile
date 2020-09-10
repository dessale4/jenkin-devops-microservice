//SCRIPTED
	// node {
	// 	echo "Build"
	// 	echo "Test"
	// 	echo "Integration Test"
	// }

//DECLARATIVE
pipeline{
	// agent any
	// agent{ docker {image 'maven:3.6.3'}}
	agent {
    docker {
        // image 'maven:3-alpine'
		image 'maven:3.6.3'
        label 'docker'
    }
}
	stages{
		stage('Build'){
			steps{
				sh "mvn --version"
				echo "Build"
			}
		}
		stage('Test'){
			steps{
				echo "Test"
			}
		}
		stage('Integration Test'){
			steps{
				echo "Integration Test"
			}
		}
	} 
	post{
		always{
			echo "I am awesom. I run always"
		}
		success{
			echo "I run only if you are successful"
		}
		failure{
			echo "I run when you fail"
		}
	}
}
