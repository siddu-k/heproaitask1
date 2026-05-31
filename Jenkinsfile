pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/siddu-k/heproaitask1.git'
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
