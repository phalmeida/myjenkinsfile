#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
        stage('Configuração') {
            steps {
                sh 'cp .env.example .env'
                sh 'composer install'
                sh 'php artisan key:generate'
            }
        }
        stage('Início'){
            steps {
                sh 'php artisan view:clear'
            }
        }
        stage("zip_archive") {
            steps {
                sh "zip -r ${env.BUILD_TAG}.zip ."
                echo "teste: ${env.BUILD_TAG}.zip"
            }
        }
    }
}