#!/usr/bin/env groovy

pipeline {
  agent {
        label 'docker' 
    }
    
    stages {
        stage('Build') {
            agent {
                docker {
                  label 'docker'
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
                  label 'docker'
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
