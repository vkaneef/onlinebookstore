pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'clean'
            }
        }
        stage('genaratin war') {
            steps {
                sh 'install'
            }
        }
     
    }
}
