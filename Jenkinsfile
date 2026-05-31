pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/username/myapp.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo Building Application...'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest'
            }
        }
    }
}
