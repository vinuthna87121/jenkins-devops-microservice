//declarative pipeline
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
				echo "Integeration Test"
			}
		}
	}

	post{
		always{
			echo 'i run always'
		}
		success{
			echo 'i run when you are successful'
		}
		failure{
			echo 'i run when anything failed'
		}
	}
}