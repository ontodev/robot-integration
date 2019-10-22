pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'cp ../ontodev_robot_master/bin/robot.jar robot.jar'
            }
        }

        stage('Test') {
            steps {
                sh 'java -jar robot.jar help'
            }
        }
    }
}

