@Library('jenkins-pipeline-shared-lib-sample')_
pipeline {
    agent any
      stages {
        stage('Print Build Info') {
            steps {
                printBuildinfo {
                name = "Sample Name"
                }
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