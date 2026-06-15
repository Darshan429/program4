pipeline {
    agent any   

    tools {
        maven 'Maven'   
    }

    stages {

        stage('Checkout') {
            steps {
                // Recommended if repo is configured in Jenkins
                checkout scm
git url: 'https://github.com/Darshan429/program4.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed'
        }
        success {
            echo 'Build SUCCESS '
        }
        failure {
            echo 'Build FAILED '
        }
    }
}
