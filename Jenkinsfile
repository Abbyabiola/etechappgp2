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
                        sh '%date% %time%'
                    }
                }
            }
        }

    }stage('5-release'){
        steps{
            sh 'pwd'
        }
    }
}