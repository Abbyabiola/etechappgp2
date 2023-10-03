pipeline {
    agent any
    stages {
        stage('1-Build') {
            steps {
                sh 'systemctl status jenkins'
            }
        }
        parallel {
            stage('parallel ') {
                stage('2-Test') {
                    steps {
                        sh 'cat /etc/passwd'
                    }
                }
                stage('3-Deploy') {
                    steps {
                        sh 'lscpu'
                        sh 'free -m'
                    }
                }
            }
            stage('release for testing') {
                parallel{
                    stage('4-release for testing') {
                        steps {
                            sh 'lscpu'
                        }
                    },
                    stage('5-release for deployment') {
                        steps {
                            sh 'free -m'
                        }
                    }
                }
                
                stage('6-production') {
                    steps {
                        sh '%date %time%'
                    }
                }
                
            }
            stage ("Securitytest") {
                steps {
                    sh 'pwd'
                }
           
               
            }
        
        }
    }
}
	
