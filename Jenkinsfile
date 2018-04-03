#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
        stage('Download') {
            steps {
                git 'https://github.com/phalmeida/pheventos.git'
            }
        }
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
          // Zip the archive to prepare it for an S3 upload
          sh "zip -r ${env.BUILD_TAG}.zip ."
        }
    }
}