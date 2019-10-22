pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'git clone https://github.com/obi-ontology/obi.git || true'
                sh 'mkdir -p obi/build'
                sh 'cp ../robot/bin/robot.jar obi/build/robot.jar'
            }
        }

        stage('Test') {
            steps {
                sh 'cd obi && make test || cd .. && rm -rf obi'
            }
        }
    }
}

