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
        stage('implantação'){
            steps {
                sh 'php artisan migrate:fresh'
                sh 'php artisan'
            }
        }
        stage('database seeder'){
             steps {
                sh 'php artisan db:seed'
            }
        }
    }
}