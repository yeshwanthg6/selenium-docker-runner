pipeline{
	agent any 
	stages{
		stage('Run Grids'){
			steps{
			sh "docker-compose -f grid.yaml up -d"
			}
		}

		stage("Run Test Suites"){
			steps{
				sh "docker-compose -f test-suites.yaml up"
			}
		}
	}

	post{
		always{
			sh "docker-compose -f grid.yaml down"
			sh "docker-compose -f test-suites.yaml down"
		}
	}
}