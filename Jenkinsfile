pipeline {
    agent any
    stages {        
        stage('Build') {
            steps {
                build 'PES1UG22CS648-1'
                sh 'g++ source.cpp -o output' //made changes
            }
        }
        
        stage('Test') {
            steps {
                sh './output'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
