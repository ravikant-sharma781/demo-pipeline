pipeline {
    agent any

    environment {
        // Define environment variables
        APP_NAME = 'my-sample-app'
        DEPLOY_ENV = 'staging'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from Git repository
                git url: 'https://github.com/ravikant-sharma781/demo-pipeline', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                // Example build step, like compiling code or creating artifacts
                echo 'Building the application...'
                // For example, if using Maven:
                // sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Example test step, like running unit tests
                echo 'Running tests...'
                // For example, if using Maven:
                // sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Example deploy step, like deploying to a staging environment
                echo "Deploying ${env.APP_NAME} to ${env.DEPLOY_ENV} environment..."
                // For example, deploy to Kubernetes or a server
            }
        }
    }

    post {
        success {
            // Actions to perform on success
            echo 'Pipeline completed successfully!'
        }
        failure {
            // Actions to perform on failure
            echo 'Pipeline failed!'
        }
        always {
            // Actions to perform always, regardless of success or failure
            echo 'Cleaning up...'
            // For example, deleting temporary files or stopping services
        }
    }
}
