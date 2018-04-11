pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {

        stage('Autogen') {
            steps {
                sh './autogen.sh'
            }
        }

        stage('Configure') {
            steps {
                sh './configure'
            }
        }
    
        stage('Build') {
            steps {
                sh 'make'
            }
        }

        stage('Check') {
            steps {
                sh 'make check'
            }
        }


    }
}
