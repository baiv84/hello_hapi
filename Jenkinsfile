#!/usr/bin/env groovy

pipeline {
  agent any
    
    stages {
        stage('Build') {
            agent {
                docker {
                  image 'node'
                  args '-u root'
                }
            }    
            
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }
        
        stage('Test') {
            agent {
                docker {
                  image 'node'
                  args '-u root'
                }
            }
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
        }
    }
}
