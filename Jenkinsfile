pipeline{
    agent any
    stages{
        stage('1-Build'){
            steps{
                sh 'systemctl status jenkins'
            }
        }
        stage('2-Test'){
            steps{
                echo "we are on parallel test"
            }
        }
        stage('parallel'){
            parallel{
                stage('3-unitest'){
                    steps{
                        sh 'df -h'
                        sh 'cat /etc/passwd'
                    }
                }
                stage('4-Deploy'){
                    steps{
                        sh 'df -h'
                    }
                }
                stage('5-Securitytest'){
                    steps{
                        sh 'pwd'
                    }
                }
            }
        }
                 stage('Production'){
                    parallel{
                        stage('6-production'){
                            steps{
                                sh 'free -m'
                            }

                        }
                    stage('7-artifact'){
                            steps{
                                echo "we are on parallel artifact"
                            }
                        }
                        stage('8-Notify'){
                            steps{
                                sh 'whoami'
                            }
                        }
                    }
                 }
                 stage('9-Release to staging'){
                    steps{
                        sh 'lscpu'
                    }
                 }
            }
        }

    

    
