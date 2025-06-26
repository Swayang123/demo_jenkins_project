pipeline {
    agent any

    options {
        disableConcurrentBuilds()
    }

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Checking out code from SCM...'
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                echo 'Running Python script...'
                sh 'python3 run_script.py'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
