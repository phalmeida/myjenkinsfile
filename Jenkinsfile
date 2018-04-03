pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '1 - Building..'
            }
        stage('Example stage 1') {
            steps {
                echo '2 - Building.. stage 1'
            }
        }
        stage('Example stage 2') {
            steps {
                echo '3 - Building.. stage 2'
            }
        }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}