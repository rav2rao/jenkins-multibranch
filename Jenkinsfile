pipeline {
    agent any
    stages {
        stage('Hello1') {
            steps {
                echo "Hello World-multibranch"
            }
        }
        stage('for the fix branch'){
            when{
                branch "multi-*"
            }
            steps{
                sh '''
                echo "This branch runs only starts with muli- "
                '''
            }
        }
        stage('pr stage'){
            when{
                branch "pr-*"
            }
            steps{
                sh '''
                echo "This branch runs only PR builds"
                '''
            }
        }    
    }
}
