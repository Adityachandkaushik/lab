pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'No build step required for static website.'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying static website...'
                // Replace this path with your local deployment path
                sh 'mkdir -p /var/www/html/static-site'
                sh 'cp -r * /var/www/html/static-site/'
            }
        }
    }

    post {
        success {
            echo '✅ Deployment successful!'
        }
        failure {
            echo '❌ Deployment failed.'
        }
    }
}
