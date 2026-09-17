pipeline {
    agent any
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['dev', 'staging', 'prod'], description: 'Select the Exam System deployment environment')
    }
    stages {
        stage('Checkout') {
            steps {
                // Change <your-github-username> to your actual GitHub username
                git branch: 'main', url: 'https://github.com<your-github-username>/Online-Exam-System.git'
            }
        }
        stage('Show Parameter') {
            steps {
                echo "Selected Examination Environment: ${params.ENVIRONMENT}"
            }
        }
        stage('Build for Environment') {
            steps {
                echo "Building the Online Examination System for the ${params.ENVIRONMENT} environment..."
            }
        }
    }
}
