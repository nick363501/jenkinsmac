@Library('jenkins-pipeline-shared-lib-sample')_
def appName = "Test Application"
pipeline {
    agent any
      stages {
        stage('Print Build Info') {
            steps {
                printBuildinfo {
                echo "${appName}"
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