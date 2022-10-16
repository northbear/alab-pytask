pipeline {
    agent {
        docker { image 'python:3.8' }
    }
    triggers{ pollSCM('H/2 * * * *') }
    stages {
        stage('Execute The Task') {
            steps {
                echo "Execute The Task"
                sh "python app/main.py"
            }
        }
    }
}
