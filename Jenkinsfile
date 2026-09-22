pipeline {

    agent any

    tools {
        jdk 'jdk17'
        maven 'maven'
    }

    stages {

        stage('Clean') {
            steps {
                sh 'mvn clean'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn package -DskipTests'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Verify') {
            steps {
                sh 'mvn verify'
            }
        }

    }

    post {

        success {
            echo 'ABC App Pipeline Successful'
        }

        failure {
            echo 'ABC App Pipeline Failed'
        }

    }

}