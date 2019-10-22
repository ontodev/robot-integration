pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'rm -rf obi'
                sh 'ls ..'
            }
        }

        stage('Test') {
            steps {
                echo 'Hello!'
            }
        }
    }
}
