pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    writeFile file: 'temp.cpp', text: '#include <iostream>\nint main() { std::cout << "PES1UG21CS627\n"; return 0; }'
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
