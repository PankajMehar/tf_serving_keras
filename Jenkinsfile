pipeline {
    agent none
    stages {
        stage('Build model serving image') {
            agent {
                dockerfile {
                    dir 'model_serving'
                    filename 'Dockerfile'
                    label 'latest'
                }
            }
        }

        stage('Build API image') {
            agent {
                dockerfile {
                    dir 'detector-api'
                    filename 'Dockerfile'
                    label 'latest'
                }
            }
        }

        stage('Build app image') {
            agent {
                dockerfile {
                    dir 'detector-app'
                    filename 'Dockerfile'
                    label 'latest'
                }
            }
        }
    }
}
