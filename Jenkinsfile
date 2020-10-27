@Library('jenkins-pipeline-shared-lib-sample')_
pipeline {
    agent any
    environment {
        appName = "Test Application Master"
    }
      stages {
        stage('Print Build Info') {
            steps {
                echo "Test Application"
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