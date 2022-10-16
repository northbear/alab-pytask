pipeline {
    agent {
        docker {
            image 'python:3.8'
        }
    }
    triggers{ pollSCM('H/5 * * * *') }
    stages {
        stage('Pull The Task') {
            steps {
                echo "Pull The Task"
                sh "python --version"
                sh "git --version"
            }
        }
        stage('Execute The Task') {
            steps {
                echo "Execute The Task"
                sh "python app/main.py"
            }
        }
    }
}
