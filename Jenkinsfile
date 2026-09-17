pipeline {
    agent any
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['dev', 'staging', 'prod'], description: 'Select the Exam System deployment environment')
    }
    stages {
        // We removed the manual checkout stage because Jenkins SCM does it automatically!
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
