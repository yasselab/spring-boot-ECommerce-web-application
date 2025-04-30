pipeline {
    agent any

    tools {
        jdk 'jdk17' // ou 'jdk11' selon ta config Jenkins
        maven 'maven3' // assure-toi que Maven est bien installé dans Jenkins
    }

    stages {
        stage('Cloner le dépôt') {
            steps {
                git 'https://github.com/Zaaim-Halim/spring-boot-ECommerce-web-application.git'
            }
        }

        stage('Compiler') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Tests') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
