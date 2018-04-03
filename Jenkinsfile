#!/usr/bin/env groovy

pipeline {
        agent any

        stages {
                stage('test') {
                        steps {
                                sh 'echo hello'
                        }
                }
                stage('test1') {
                        steps {
                                sh 'echo $TEST'
                        }
                }
                stage('test3') {
                        steps {
                                script {
                                        if (env.BRANCH_NAME == 'master') {
                                                echo 'I only execute on the master branch ${env.BRANCH_NAME}'
                                        } else {
                                                echo 'I execute elsewhere ${env.BRANCH_NAME}'
                                        }
                                }
                        }
                }
        }
}