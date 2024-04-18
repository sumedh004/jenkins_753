pipeline{

    agent any 

    stages{
        stage('Build'){
            steps{
                
                echo "In Build stage, source code is compiled and packaged into executable files"
                echo "Ant is a tool that can be used for build stage"
            }

        }

        stage('Unit and Integration Tests'){
           steps{

                echo "unit tests verifies functionality of individual functions and integration test makes sure that all modules interact with each other without any issues"
                echo "JUnit and Selenium can be used for testing"
            }

            post {
                success {
                    //emailext (attachLog: true, body: 'Build is $BUILD_STATUS', subject: 'Build Status', to: 'sumedhvartak@outlook.com')
                    emailext(to: 'sumedhvartak@outlook.com',
                             subject: 'Build Status for Unit and Integration Tests',
                             body: 'Build is $BUILD_STATUS',
                             attachLog: true)
                 }

                failure {
                    emailext(to: 'sumedhvartak@outlook.com',
                             subject: 'Build Status for Unit and Integration Tests',
                             body: 'Build is $BUILD_STATUS',
                             attachLog: true)
                 }
             }

        }

        stage('Code analysis'){
            steps{
                
                echo "Analyses the code for any issues, checks quality of code"
                echo "SonarQube can be used for code analysis"
            }
        }

        stage('Security scan'){
            steps{
                
                echo "This stage checks for security vulnerabilities, any loopholes or exploit present within the code"
                echo "Intruder, SonarQube, OWASP Zap can be used for security scanning"
            }   
        

            post {
                success {
                    //emailext (attachLog: true, body: 'Build is $BUILD_STATUS', subject: 'Build Status', to: 'sumedhvartak@outlook.com')
                    emailext(to: 'sumedhvartak@outlook.com',
                             subject: 'Build Status for security scan',
                             body: 'Build is $BUILD_STATUS',
                             attachLog: true)
                 }

                failure {
                    //emailext (attachLog: true, body: 'Build is $BUILD_STATUS', subject: 'Build Status', to: 'sumedhvartak@outlook.com')
                    emailext(to: 'sumedhvartak@outlook.com',
                             subject: 'Build Status for security scan',
                             body: 'Build is $BUILD_STATUS',
                             attachLog: true)
                 }
             }
        }
        
        
        stage('Deploy to Staging'){
            steps{
                
                echo "Staging environment is a cpoy of production environment where the application is deployed to check and test the working of it before finalizing it to production environment"
                echo "AWS CodeDeploy, codecommit and codepipeline can be used for deploying"
            }
        }

        stage('Integration tests on Staging'){
            steps{

                echo "Testing on staging environment is performed to ensure the application is performing as expected"
                echo "Postman is a tool that can be used"
            }

            post {
                success {
                    //emailext (attachLog: true, body: 'Build is $BUILD_STATUS', subject: 'Build Status', to: 'sumedhvartak@outlook.com')
                    emailext(to: 'sumedhvartak@outlook.com',
                             subject: 'Build Status for Integration tests on Staging',
                             body: 'Build is $BUILD_STATUS',
                             attachLog: true)
                 }

                failure {
                    //emailext (attachLog: true, body: 'Build is $BUILD_STATUS', subject: 'Build Status', to: 'sumedhvartak@outlook.com')
                    emailext(to: 'sumedhvartak@outlook.com',
                             subject: 'Build Status for Integration tests on Staging',
                             body: 'Build is $BUILD_STATUS',
                             attachLog: true)
                 }
             }

        }
        stage('Deploy to Production'){
            steps{
                echo "The application is deployed to live to production server where the users can access it"
                echo "Same tools in deploying to staging can be used"
            }
        }
    }
}
