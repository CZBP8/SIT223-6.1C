pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo 'Building...'
                echo 'Tool: Maven'
            }
        }
        stage("Unit and Integration Tests") {
            steps {
                echo 'Running Unit and Integration Tests...'
                echo 'Tool: JUnit'
            }
        }
        stage("Code Analysis") {
            steps {
                echo 'Performing Code Analysis...'
                echo 'Tool: SonarQube'
            }
        }
        stage("Security Scan") {
            steps {
                echo 'Running Security Scan...'
                echo 'Tool: OWASP ZAP'
            }
        }
        stage("Deploy to Staging") {
            steps {
                echo 'Deploying to Staging...'
                echo 'Environment: AWS EC2'
            }
        }
        stage("Integration Tests on Staging") {
            steps {
                echo 'Running Integration Tests on Staging...'
                echo 'Tool: Integration testing script or tool'
            }
        }
        stage("Deploy to Production") {
            steps {
                echo 'Deploying to Production...'
                echo 'Environment: AWS EC2 (or another production server)'
            }
        }
    }

    post {
        success {
            mail to: "l2835456485@gmail.com",
                subject: "Pipeline Success",
                body: "The pipeline completed successfully!"
        }
        failure {
            mail to: "l2835456485@gmail.com",
                subject: "Pipeline Failure",
                body: "The pipeline failed."
        }
    }
}
