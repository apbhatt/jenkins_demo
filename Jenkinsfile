pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from your version control system (e.g., Git)
                // You may need to configure credentials for authentication
                // new comment to test ngrok w webhook
                checkout scm
                sh 'echo "step 1"'
            }
        }
        
        stage('Build') {
            steps {
                // Compile and package your Java application
                //sh 'javac -version'
                //sh 'mvn clean package'
                sh 'echo "step 2"'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests on your application
                //sh 'mvn test'
                sh 'echo "step 3"'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy your application (e.g., to a web server or application server)
                // This is a placeholder; actual deployment steps depend on your infrastructure
                sh 'echo "Deploying the application"'
            }
        }
    }
    
    post {
        success {
            // If all stages are successful, you can perform additional actions here
            echo 'Pipeline completed successfully!'
        }
        
        failure {
            // If any stage fails, you can perform cleanup or notifications here
            echo 'Pipeline failed! Please investigate.'
        }
    }
}
