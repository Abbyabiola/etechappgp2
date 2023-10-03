pipeline{
	agent any
	stages{
		stage('Build'){
			steps{
				sh 'systemctl status jenkins'
			}
		}
		stage('Test'){
			parallel {
				stage ('unitest'){
					steps {
						sh 'df -h'
						sh 'cat /etc/passwd'
					}

				}
				
			}
		}
		stage('Deploy'){
			steps{
				sh'ls -l'
			}
		}
		stage('Regression test'){
			parallel {
				stage ('rebtest'){
					steps{
						sh 'lscpu'
					}

				}
					
				stage('Release to production'){
					steps{
						sh 'free -m'
				}
				
			}
			}
			stage('Notify'){
				steps{
					sh '%date% %time%'
				}
			}
			stage('Securitytest'){
				steps{
					sh 'pwd'
				}
			}
		}
}
}

	
