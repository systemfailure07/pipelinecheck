pipeline {
    agent any

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
        failure {
            echo 'ABC App Pipeline Failed'
        }
    }
}