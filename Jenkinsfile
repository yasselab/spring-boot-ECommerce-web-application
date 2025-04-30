pipeline {
    agent any

    stages {
        stage('Cloner le dépôt') {
            steps {
                git 'https://github.com/yasselab/spring-boot-ECommerce-web-application.git'
            }
        }

        stage('Compiler') {
            steps {
                sh './mvnw clean compile'
            }
        }

        stage('Tests') {
            steps {
                sh './mvnw test'
            }
        }

        stage('Package') {
            steps {
                sh './mvnw package'
            }
        }
    }
}
