pipeline {
    agent any
    environment {
        DIRECTORY_PATH = "${WORKSPACE}"
        TESTING_ENVIRONMENT = 'staging'
        PRODUCTION_ENVIRONMENT = 'Betty Sun'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Fetching the source code from ${DIRECTORY_PATH}'
                echo 'Compiling the code and generating necessary artifacts'
            }
        }
        stage('Test') {
            steps {
                echo 'Running unit tests'
                echo 'Running integration tests'
            }
        }
        stage('Code Quality Check') {
            steps {
                echo 'Checking the quality of the code'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application to ${TESTING_ENVIRONMENT} environment'
            }
        }
        stage('Approval') {
            steps {
                script {
                    sleep 10  
                }
                echo 'Manual approval received'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to ${PRODUCTION_ENVIRONMENT} environment'
            }
        }
    }
}
