pipeline {
    agent any
    environment {
        DIRECTORY_PATH="C:\\Users\\sharni\\code"
        TESTING_ENVIRONMENT= "sharni_stg"
        PRODUCTION_ENVIRONMENT= "sharni_prod"
    }
    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from the directory $DIRECTORY_PATH"
                echo "Compile the code and generate any necessary artifacts"
            }
        }
        stage('Test') {
            steps {
                echo 'Unit Tests'
                echo "Integration Tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
        stage('Deploy to Testing') {
            steps {
                echo "Deploy the application to a testing environment: $TESTING_ENVIRONMENT"
            }
        }
        stage('Approval') {
            steps {
                sleep 10
                echo 'Approved'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploy the application to a production environment: $PRODUCTION_ENVIRONMENT"
            }
        }
    }
}
