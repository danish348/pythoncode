pipeline {
    agent any
    
    stages {

        stage('Build') {
            steps {
                script {
                    sh 'apt-get update'
                    sh 'apt-get upgrade -y'
                    
                }
            }
        }
        stage('Test') {
            steps {
                script {

                    sh 'apt-get update'
                    sh 'apt-get upgrade -y'
                    sh 'apt-get install -y python3 python3-venv python3-pip'

                    sh '''
                        python3 -m venv .venv
                        . .venv/bin/activate

                        sleep 15
                        python test.py
                        '''
                }
            }
        }
    }
}
