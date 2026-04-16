pipeline {
    agent any

    tools {
        maven 'Maven'   // Must match Jenkins tool name
    }

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/<your-username>/MyMavenGuavaApp.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
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
