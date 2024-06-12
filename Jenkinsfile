pipeline {
    agent {
        label 'node-1'
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo this is Build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo this is Test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo this is Deploy'
            }
        }
    }
}