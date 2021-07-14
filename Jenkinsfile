pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                echo "Git checkout for bat files"
                git 'https://github.com/mj07yadav/Pipeline_Script.git'
            }
        }
        stage('Build') {
            steps {
                bat 'Build.bat'
            }
        }
        stage('Unit Test') {
            steps {
                bat 'Unit.bat'
            }
        }
        stage('Quality') {
            steps {
                bat 'Quality.bat'
            }
        }
        stage('Deploy') {
            steps {
                bat 'Unit.bat'
            }
        }
    }
    post {
        always {
            echo "this will run always no matter what"
        }
        success {
            echo "this will run only when build is successful"
        }
        failure {
            echo "this will run when build is failed"
        }
        unstable {
            echo "this will run when build is unstable"
        }
        changed {
            echo "this will run when something is changed from previous build"
        }
    }
}
