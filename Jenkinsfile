pipeline {
    agent any

    tools {
        maven 'Maven 3.9'
    }

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/your-username/demo-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar'
            }
        }

        stage('Run App') {
            steps {
                sh 'java -jar target/manual-app-1.0.jar'
            }
        }
    }
}
