@Library('testcut@master') _
pipeline {
    agent any
      stages {
        stage('Test') {
            steps {
                echo "Jenkinsfile"
                testcut.cuturl
            }
        }
    }
}