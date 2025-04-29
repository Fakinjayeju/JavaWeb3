pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh"""
                mvn package
                """
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}