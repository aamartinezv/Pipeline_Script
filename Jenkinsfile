pipeline{
	agent none
	stages{
		stage('Non-Parallel Stage'){
			agent {	
				label "Master"
			}
			steps{
				echo 'This stage will be executed first'
			}
			
		}
		stage('Run Tests'){
			parallel{
				stage('Test on Windows'){
					agent{
						label "Windows_Node_A1"
					}
					steps{
						echo "Task 1 on Agent"
					}
				}
				stage('Test on Master'){
					agent{
						label "Master"
					}
					steps{
						echo "Task 1 on Agent"
					}
				}
			
			}
		}
		
	}
}
