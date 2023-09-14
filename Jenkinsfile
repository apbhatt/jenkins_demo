pipeline {
    agent any

    stages {
        stage('Create Directory and File') {
            steps {
                sh 'mkdir mydir' // Create a directory
                sh 'echo "Hello, Jenkins!" > mydir/myfile.txt' // Create and write to a file
            }
        }

        stage('List Files') {
            steps {
                sh 'ls -al mydir' // List files in the directory
            }
        }

        stage('Append to File') {
            steps {
                sh 'echo "Appending more content." >> mydir/myfile.txt' // Append to the existing file
            }
        }

        stage('Read File') {
            steps {
                sh 'cat mydir/myfile.txt' // Read and print the file content
            }
        }

        stage('Delete Directory') {
            steps {
                sh 'rm -rf mydir' // Delete the directory and its contents
            }
        }
    }
    
    post {
        success {
            echo 'File operations completed successfully.'
        }
        failure {
            echo 'File operations failed.'
        }
    }
}
