pipeline{
	agent any 
	stages{
		stage('Run Test'){
			steps{
			sh "docker-compose up"
			}
		}

		stage("Tear Down Grid"){
			steps{
				sh "docker-compose down"
			}
		}
	}
}