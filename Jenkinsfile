pipeline {
    agent any

    stages {
        stage('Build') {
            when {
                branch 'main'
            }
            steps {
                echo 'Building application'
            }
        }

        stage('Test') {
            when {
                anyOf {
                    branch 'feature/*'
                    branch 'release/*'
                }
            }
            steps {
                echo 'Running tests'
            }
        }

        stage('Security Scan') {
            when {
                branch 'release/*'
            }
            steps {
                echo 'Running security scan'
            }
        }
    }
}
