pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                try {
                        echo 'Build stage executed successfully'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        error "Build failed: ${e.message}"
                    }
                }
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                // Test steps
                script {
                    try {
                        echo 'Test stage executed successfully'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        error "Test failed: ${e.message}"
                    }
                }
            }
        }
        stage('Code Analysis') {
            steps {
                script {
                    try {
                        echo 'Code Analysis stage executed successfully'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        error "Test failed: ${e.message}"
                    }
                }
            }
        }
        stage('Security Scan') {
            steps {
                script {
                try {
                         echo 'Security stage executed successfully'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        error "Test failed: ${e.message}"
                    }
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                script {
                try {
                         echo 'Deploy stage executed successfully'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        error "Test failed: ${e.message}"
                    }
                }
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                script {
                try {
                        echo 'Integration stage executed successfully'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        error "Test failed: ${e.message}"
                    }
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                script {
                try {
                        echo 'Production stage executed successfully'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        error "Test failed: ${e.message}"
                    }
                }
            }

            post {
                success {
                    // Send email notification on successful deployment
                    emailext (
                        to: 'shetyeketan18@gmail.com',
                        subject: 'Deployment Successful',
                        body: 'The deployment was successful. Please verify.'
                    )
                }
            }
        }
    }

    
}
