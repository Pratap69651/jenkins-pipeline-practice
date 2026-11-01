
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building application'
                sh 'chmod +x app.sh'
                sh './app.sh'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                sh 'test -f app.sh'
                sh 'grep -q "Hello from Jenkins CI/CD Pipeline" app.sh'
                echo 'All tests passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment simulation completed!'
            }
        }
    }
}
