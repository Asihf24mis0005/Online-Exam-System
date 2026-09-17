pipeline {
    agent any
    stages {
        stage('Generate Exam Report') {
            steps {
                bat 'python app.py'
            }
        }
        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'exam_report.txt', fingerprint: true
            }
        }
    }
}
