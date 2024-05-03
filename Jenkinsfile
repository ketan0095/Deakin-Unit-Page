pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Build the code using Maven or another build automation tool
                echo "Build Stage"
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                // Run unit tests using JUnit or another test automation tool
                // Run integration tests using Selenium or another integration testing tool
                echo "Testing Stage"
            }
        }
        stage('Code Analysis') {
            steps {
                // Integrate a code analysis tool like SonarQube or Checkstyle
                echo "Code Analysis Stage"
            }
        }
        stage('Security Scan') {
            steps {
                // Perform a security scan using tools like OWASP ZAP or SonarQube
                echo "Security Stage"
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Deploy the application to a staging server, e.g., AWS EC2 instance
                echo "Deployment Stage"
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // Run integration tests on the staging environment
                echo "Integration Stage"
            }
        }
        stage('Deploy to Production') {
            steps {
                // Deploy the application to a production server, e.g., AWS EC2 instance
                echo "Production Stage"
            }

            // post {
            //     success {
            //         // Send email notification on successful deployment
            //         emailext (
            //             to: 'shetyeketan18@gmail.com',
            //             subject: 'Deployment Successful',
            //             body: 'The deployment was successful. Please verify.'
            //         )
            //     }
            // }
        }
    }


    post{
        always{
            echo 'Pipeline Completed.'
        }

        success{
            emailext body:'Pipeline succeeded. All stages complted.',
                     subject: 'Pipeline status: Successful',
                     to:'shetyeketan18@gmail.com',
                     attachmentsPattern: 'build/**/*.log'
        }

        failure{
            emailext body:'Pipeline failed. Check logs for detail',
                     subject: 'Pipeline status: Failure',
                     to:'shetyeketan18@gmail.com',
                     attachmentsPattern: 'build/**/*.log'
        }
    }
}
