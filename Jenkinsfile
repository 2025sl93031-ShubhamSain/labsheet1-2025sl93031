pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/2025sl93031-ShubhamSain/labsheet1-2025sl93031.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Build running"'
            }
        }

        stage('Test') {
            steps {
                sh '''
                python3 - <<EOF
import calculator

assert calculator.add(2,3) == 5
assert calculator.subtract(5,3) == 2
assert calculator.multiply(2,3) == 6

print("All tests passed")
EOF
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploy placeholder"'
            }
        }
    }
}
