pipeline{
	agent any
	stages{
		stage('1-Build'){
			steps{
				sh 'systemctl status jenkins'
			}
		}
		stage('2-Test'){
			parallel {
				stage ('unitest'){
					steps {
						sh 'df -h'
						sh 'cat /etc/passwd'
					}

				}
				
			}
		}
		stage('3-Deploy'){
			steps{
				sh'ls -l'
			}
		}	
		stage('4-Release to staging'){
					steps{
						sh 'free -m'
				}
				
			}
			
			stage('5-Notify'){
				steps{
					sh '%date% %time%'
				}
			}
            stage('6-parallel') {
                parallel {
                    stage ('unitest'){
                        steps{
                            sh 'df -h'
                            sh 'cat /etc/passwd'
                        }
                    }
                }
			stage('7-Securitytest'){
				steps{
					sh 'pwd'
				}
            }
            stage('8-Release to production'){
                steps{
                      echo "end of pipeline" 
            }
                
           }
    	}
    }
}



	
