pipeline {
    agent { label 'local-node1' }

    environment {
        NODE_ENV = 'development'
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/saranvoyage-cpu/my-react-app.git', branch: 'main'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test (optional)') {
            steps {
                sh 'npm test || true'
            }
        }
    }
}
