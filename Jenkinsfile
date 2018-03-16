pipeline {
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
            }
        }
        stage('Staging') {
            when {
                branch 'dev'
            }
            steps {
            }
        }
        stage('Prod') {
            when {
                branch 'master'
            }
            steps {
            }
        }
    }
}