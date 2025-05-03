pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout the code from GitHub
                    git branch: 'main', url: 'https://github.com/Rajeevkr18/cicdjankin.git'
                }
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building HTML project...'
                // Add any build steps if you need (e.g., minifying, bundling)
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                // You can add steps to deploy your project, for example:
                // - Push to a server
                // - Upload to GitHub Pages
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running tests (if any)...'
                // You can add steps to run tests if you have any (unit tests, etc.)
            }
        }
    }
    
    post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build or deployment failed!'
        }
    }
}
