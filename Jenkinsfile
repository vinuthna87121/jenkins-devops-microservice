//declarative pipeline
pipeline{
	 agent any
	 environment{
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH= "$dockerHome/bin:$mavenHome/bin:$PATH"
	 }
	 //{
    //     docker {
    //         image 'maven:3.9.9'
    //     }
    // }
	stages{
		stage('CheckOut'){
			steps{
				sh 'mvn --version'
				sh 'docker version'
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
		stage('Compile'){
			steps{
				sh "mvn clean compile"
			}
		}
		stage('Test'){
			steps{
				sh "mvn test"
			}
		}
		stage('Integration Test'){
			steps{
				sh "mvn failsafe:Integration-test failsafe:verify"
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