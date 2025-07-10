pipeline {
    agent any

    tools {
        maven 'M32'   // Make sure this Maven version is configured in Jenkins
             // Make sure this JDK version is configured in Jenkins
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
