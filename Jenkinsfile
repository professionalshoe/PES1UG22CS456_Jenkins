pipeline{
	agent any
	stages{
//		stage('clone repository'){
//			steps{
//				checkout(
//				git branch: "main",
//				url:"https://github.com/professionalshoe/PES1UG22CS456_Jenkins.git"
//			}
//		}
		stage('Build'){
			steps{
				build 'PES1UG22CS456-1'
				sh 'g++ main.cpp -o output'
			}
		}
		
		stage('Test'){
			steps{
				sh './output'
			}
		}
		
		stage('Deploy'){
			steps{
				echo 'deployed'
			}
		}
	}
	post{
		failure{
			echo 'Pipeline Failed'
		}
	}
}
