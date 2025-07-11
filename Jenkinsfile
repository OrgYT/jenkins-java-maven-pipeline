pipeline {
    agent any

    tools {
        maven 'Maven382' // Ensure this version is configured in Jenkins
            // Ensure this JDK version is configured in Jenkins
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
                sleep 300s
                // Run unit tests
                sh 'mvn test'
            }
        }


