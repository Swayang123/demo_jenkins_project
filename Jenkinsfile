pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Cloning the repository...'
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh 'pip install -r requirements.txt || true'
            }
        }

        stage('Run Script') {
            steps {
                echo 'Running script...'
                sh 'python3 script.py'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}
