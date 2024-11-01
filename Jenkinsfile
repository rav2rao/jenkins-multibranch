pipeline {
    agent any
    stages {
        stage('Hello1') {
            steps {
                echo "Hello World-multibranch"
            }
        }
        stage('fix branch build') {
            when {
                branch "fix-*"
            }
            steps {
                sh '''
                echo "This stage build only fix branches"
                '''
            }
        }
        stage('PR build branch') {
            when {
                branch "PR-*"
            }
            steps{
                sh '''
                echo "This build only PR's "
                '''
            }
        }
    }
}
