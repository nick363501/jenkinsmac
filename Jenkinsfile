@Library('jenkins-pipeline-shared-lib-sample')_
pipeline {
    agent any
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