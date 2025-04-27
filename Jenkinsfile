#!/usr/bin/env groovy

//-----
pipeline {
    agent any
    stages {
        stage('Verify Docker') {
            steps {
                script {
                    sh 'docker --version'
                }
            }
        }
    }
}
