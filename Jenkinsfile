pipeline {
    agent any

    tools {
        maven 'M32' // Ensure this Maven version is configured in Jenkins
        // Note: Add JDK configuration here if needed
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from SCM
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Build the project using Maven
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                
                // Run unit tests
                sh 'mvn test'
            }
        }
    }
}
