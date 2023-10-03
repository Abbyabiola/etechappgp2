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
		stage('Release to production'){
					steps{
						sh 'free -m'
				}
				
			}
			
			stage('Notify'){
				steps{
					sh '%date% %time%'
				}
			}
            stage('parallel'){
                parallel {
                    stage ('unitest'){
                        steps{
                            sh 'df -h'
                            sh 'cat /etc/passwd'
                        }
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



	
