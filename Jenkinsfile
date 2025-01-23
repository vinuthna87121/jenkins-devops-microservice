//declarative pipeline
pipeline{
	agent {docker { image:'maven:3.9.9'}}
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
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