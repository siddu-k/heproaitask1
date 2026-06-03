pipeline { 
    agent any 
 
    stages { 
 
        stage('Checkout') { 
            steps { 
                git branch: 'main', 
                url: 'https://github.com/username/myapp.git' 
            } 
        } 
 
        stage('Test') { 
            steps { 
                sh 'pytest' 
            } 
        } 
 
        stage('Build Docker Image') { 
            steps { 
                sh 'docker build -t siddu99/myapp:latest .' 
            } 
        } 
 
        stage('Push Image') { 
            steps { 
                sh 'docker push siddu99/myapp:latest' 
            } 
        } 
 
        stage('Deploy to Staging') { 
            steps { 
                sh 'docker-compose -f docker-compose.staging.yml up -d' 
            } 
        } 
    } 
}
