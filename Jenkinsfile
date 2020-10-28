@Library('jenkins-pipeline-shared-lib-sample@newFeature')_
pipeline {
    agent any
    environment {
        appName = "Test Application"
    }
      stages {
        stage('Print Build Info') {
            steps {
                echo "${appName}"
                cuturl()
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