pipeline {
    agent any
    stages {
        stage('Parallel Integrity Checks') {
            parallel {
                stage('Frontend Portal Check') {
                    steps {
                        bat 'python frontend_check.py'
                    }
                }
                stage('Backend Evaluation Check') {
                    steps {
                        bat 'python backend_check.py'
                    }
                }
            }
        }
        stage('Summary') {
            steps {
                echo 'Both Exam Frontend UI and Evaluation Backend engines are verified.'
            }
        }
    }
}
