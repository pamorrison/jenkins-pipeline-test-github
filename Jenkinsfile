pipeline {
    agent none
    
    stages {
    
        stage ('stage 1') {
        
            agent {
                docker {
                    image 'lfoppiano/grobid:0.5.5'
                    args '-d -t --init -p --name grobid_cont 8080:8080 -p 8081:8081'
                }
            }
            steps {
                sh 'echo hello'
                sh 'docker export docker export -o="$(pwd)/thing.tar" grobid_cont
            }
        }
    }
}