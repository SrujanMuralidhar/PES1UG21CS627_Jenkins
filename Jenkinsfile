pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG21CS627 temp.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG21CS627'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deployment steps go here'
                }
            }
        }
    }

    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
