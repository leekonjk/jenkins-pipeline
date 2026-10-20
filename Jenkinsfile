
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting build stage'
                sh 'python3 -m compileall -q .'
            }
        }

        stage('Test') {
            steps {
                echo 'Starting test stage'
                sh 'python3 -m unittest discover -s tests'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Starting deployment stage'
                echo 'Deployment command goes here'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed. Check the stage logs.'
        }
    }
}
