pipeline {
    agent none
    
    stages {
    
        stage ('stage 1') {
        
            agent {
                docker {
                    image 'lfoppiano/grobid:0.5.5'
                    args '-d -t --init --rm -p 8080:8080 -p 8081:8081'
                }
            }
            steps {
                sh {'echo hello'}
            }
        }
    }
}