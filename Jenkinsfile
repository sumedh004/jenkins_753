pipeline{

    agent any 

    stages{
        stage('Build'){
            steps{

            // echo "Fetch the source code from $DIRECTORY_PATH"
            echo "Ant is a tool that can be used for build stage"
            }

        }

        stage('Unit and Integration Tests'){
           steps{

            // echo "unit tests"
            echo "Selenium can be used for testing"
            }

        }

        stage('Code analysis'){
            steps{

            //echo "check the quality of code"
            echo "SonarQube can be used for code analysis"
            }
        }

        stage('Security scan'){
            steps{
            //echo "deploy the application to a $TESTING_ENVIRONMENT environment"
                echo "Intruder, SonarQube, OWASP Zap can be used for security scanning"
            }
        }
        
        stage('Deploy to Staging'){
            steps{
            //echo "deploy the application to a $TESTING_ENVIRONMENT environment"
                echo "Deploying to Azure VM server"
            }
        }

        stage('Approval'){
            steps{

            sleep(10)
            }

        }
        stage('Deploy to Production'){
            steps{
            
            //echo "deploy to $PRODUCTION_ENVIRONMENT environment"
            }
        }
    }
}
