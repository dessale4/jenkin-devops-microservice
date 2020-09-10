//SCRIPTED
	// node {
	// 	echo "Build"
	// 	echo "Test"
	// 	echo "Integration Test"
	// }

//DECLARATIVE
pipeline{
	agent any
	stages{
		stage('Build'){
			steps{
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
		always{
			echo "I run when you fail"
		}
	}
}
