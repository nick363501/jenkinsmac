@Library('jenkins-pipeline-shared-lib-sample@master')_
pipeline {
    agent any
    environment {
        appName = "Test Application"
    }
      stages {
        stage('Print Build Info') {
            steps {
                echo "${appName}"ß
            }
        }
        
        stage('Disable balancer') {
            steps {
                disableBalancerUtils()
            }
        }
        

        stage('Deploy') {
            steps {
                deploy()
            } 
        }
        stage('Enable balancer') {
            steps {
                enableBalancerUtils()
            }
        } 
        
        stage('Check Status') {
            steps {
                checkStatus()
            }
        }
      }
}
