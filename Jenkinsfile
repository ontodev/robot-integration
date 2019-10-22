pipeline {
    agent any

    stages {
        stage('OBI') {
            steps {
                script {
                    try {
                        sh 'git clone https://github.com/obi-ontology/obi.git'
                        sh 'mkdir -p obi/build'
                        sh 'cp ../ontodev_robot_master/bin/robot.jar obi/build/robot.jar'
                        sh 'cd obi && make test'
                    } finally {
                        sh 'rm -rf obi'
                    }
                }
            }
        }
    }
}

