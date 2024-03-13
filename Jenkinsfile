pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from your repository
                git 'https://github.com/achrafwe/TP4IPS.git'
            }
        }
        
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
        
        stage('Package') {
            steps {
                // Package your application using Maven
                sh 'mvn package'
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
