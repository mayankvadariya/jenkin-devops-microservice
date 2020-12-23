//Scripted pipeline  OLD way of working with jenkins file
// node {
// 		echo "Build"
// 		echo "Test"
// 		echo "Integration Test"
	
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
	} post{
		always{echo 'I run always!'}
		success{
			echo 'I run when you succeed'
		}
		failure{
			'Build failed'
		}
	}
}