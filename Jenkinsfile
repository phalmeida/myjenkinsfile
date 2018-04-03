#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
        stage('Build') {
            stage('Example stage 1') {
                echo '1 - Building..'
            }
            stage('Example stage 2') {
                echo '2 - Building..'
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