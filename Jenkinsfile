pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'rm -rf robot.jar'
                sh 'ln -snf ../ontodev_robot_master/bin/robot.jar robot.jar'
            }
        }

        stage('Test') {
            steps {
                sh 'java -jar robot.jar help'
            }
        }
    }
}

