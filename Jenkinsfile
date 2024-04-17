pipeline{

    agent any 

    environment{
        DIRECTORY_PATH = "C:\\Users\\sumedh\\Downloads"
        TESTING_ENVIRONMENT = "test"
        PRODUCTION_ENVIRONMENT = "sumedh"
    }

    stages{
        stage('Build'){
            steps{

            echo "Fetch the source code from $DIRECTORY_PATH"
            echo "compile the code and generate any necessary artifacts"
            }

        }

        stage('Test'){
           steps{

            echo "unit tests"
            echo "integration tests"
            }

        }

        stage('Code Quality Check'){
            steps{

            echo "check the quality of code"
            }
        }

        stage('Deploy'){
            steps{
            echo "deploy the application to a $TESTING_ENVIRONMENT environment"
            }
        }

        stage('Approval'){
            steps{

            sleep(10)
            }

        }
        stage('Deploy to Production'){
            steps{
            
            echo "deploy to $PRODUCTION_ENVIRONMENT environment"
            }
        }
    }
}
