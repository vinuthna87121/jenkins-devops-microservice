//declarative pipeline
pipeline{
	 agent any
	 //{
    //     docker {
    //         image 'maven:3.9.9'
    //     }
    // }
	stages{
		stage('Build'){
			steps{
				//sh 'mvn --version'
				echo "Build"
				echo "$PATH"
				echo "BUILD_NUMBER-$env.BUILD_NUMBER"
				echo "BUILD_ID-$env.BUILD_ID"
				echo "BUILD_NUMBER-$env.BUILD_NUMBER"
				echo "JOB_NAME-$env.JOB_NAME"
				echo "BUILD_TAG-$env.BUILD_TAG"
				echo "BUILD_URL-$env.BUILD_URL"

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