pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                checkout scm
            }
        }
        stage('Dev') {
            when {
                branch 'dev'
            }
            steps {
                echo 'Dev'
            }
        }
        stage('Staging') {
            when {
                branch 'staging'
            }
            steps {
                echo 'Staging'
            }
        }
        stage('Prod') {
            when {
                branch 'master'
            }
            steps {
                echo 'Prod'
            }
        }
    }
}