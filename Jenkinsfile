#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
        stages('Build') {
            stage('Example stage 1') {
                steps {
                    echo '1 - Building..'
                }
            }
            stage('Example stage 2') {
                steps {
                    echo '2 - Building..'
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