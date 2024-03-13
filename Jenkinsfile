pipeline {
    agent any        
        stage('Build') {
            steps {
                // Compile your Java project using Maven
                sh 'mvn clean compile'
            }
        }
        
        stage('Test') {
            steps {
                // Run your tests using Maven
                sh 'mvn test'
            }
        }
        
        stage('Deploy') {
            steps {
                // Add your deployment steps here
                // For example, deploying your application to a server
                sh 'echo "Deploying..."'
            }
        }
    }
    
    post {
        always {
            // Clean up any temporary files or resources
            cleanWs()
        }
    }
}
