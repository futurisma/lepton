pipeline {
    agent {
        docker {
            image 'ubuntu/build'
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
