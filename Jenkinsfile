pipeline {
    agent none
    
    stages {
    
        stage ('stage 1') {
        
            agent {
                docker {
                    image 'lfoppiano/grobid:0.5.5'
                    args '-d -t --init --name grobid_cont -p 8080:8070 -p 8081:8071'
                }
            }
            steps {
                sh 'echo hello'
                sh 'docker export -o="$(pwd)/thing.tar" grobid_cont'
            }
        }
    }
}