pipeline {
    agent any

    stages {
        stage('OBI') {
            steps {
                try {
                    sh 'git clone https://github.com/obi-ontology/obi.git'
                    sh 'mkdir -p obi/build'
                    sh 'ln -snf ../ontodev_robot_master/bin/robot.jar obi/build/robot.jar'
                    sh 'cd obi && make test'
                } finally {
                    sh 'rm -rf obi'
                }
            }
        }
    }
}

