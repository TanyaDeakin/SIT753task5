pipeline {
    agent any

    environment {
        DIRECTORY_PATH = "C:/ProgramData/Jenkins/.jenkins/workspace/Task5Pipeline"
        TESTING_ENVIRONMENT = "DeakinTesting"
        PRODUCTION_ENVIRONMENT = "TanyaGujral"
    }

    stages {
        stage('Build') {
            steps {
                echo "In Build stage"
                echo "Fetch the source code from the directory path specified by the path: : ${env.DIRECTORY_PATH}"
            }
        }

        stage('Test') {
            steps {
                echo "In Test Stage"
                echo "Unit tests"
                echo "Integration tests"
            }
        }

        stage('Code Quality Check') {
            steps {
                echo "In Code Quality Check Stage"
                echo "Check the quality of the code"
            }
        }

        stage('Deploy') {
            steps {
                echo "In Deploy Stage"
                echo "Deploy the application to the ${env.TESTING_ENVIRONMENT} environment"
            }
        }

        stage('Approval') {
            steps {
                script {
                    echo "In Approval Stage"
                    echo "Paused 10 seconds before continuing"
                    sleep(time: 10, unit: 'SECONDS')
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "In Deploy to Production Stage"
                echo "Deploy the code to the ${env.PRODUCTION_ENVIRONMENT} environment"
            }
        }
    }
}
