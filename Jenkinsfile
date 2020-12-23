//Scripted pipeline  OLD way of working with jenkins file
// node {
// 		echo "Build"
// 		echo "Test"
// 		echo "Integration Test"
	
// }

//DECLARATIVE

pipeline{
	agent any
	//agent { docker { image 'maven:3.6.3' } }
	stages{
		stage('Build'){
			steps{
				echo "Build"
				//sh "mvn --version"
				echo "Build number - $env.Build_NUMBER"
				echo "Build id - $env.Build_ID"
				echo "Job name - $env.JOB_NAME"
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
		always{echo 'I run always!'}
		success{
			echo 'I run when you succeed'
		}
		failure{
			echo 'Build failed'
		}

		//changed - When status changes from failure to success or visa versa
		//unstable - When test case fails
	}
}