pipeline {
    agent any
    
    stages {
        stage ('create network') {
            steps {
                sh 'docker network create my_net'
            }
        }
    
        stage ('parallel') {
        
            agent {
                docker {
                    image 'lfoppiano/grobid:0.5.5'
                    args '-d -t --init --name grobid_cont -p 8080:8070 -p 8081:8071 -v /Users/"Paul Morrison"/cont-data:/data'
                }
            }
            steps {
                sh 'echo "hello" > /data/test.txt'
            }
        }
    }
}