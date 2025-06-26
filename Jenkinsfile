pipeline {
    agent any

    options {
        disableConcurrentBuilds()
    }

    stages {
        stage('Checkout Code') {
            steps {
                script {
                    echo 'Simulating checkout (code is local)'
                    sh 'ls -l'
                }
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    echo 'Running Python script...'
                    sh 'python3 run_script.py'
                }
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