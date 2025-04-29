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
            stage('Upload Artifact') {
            steps {
                sh"""
                cd target
                aws s3 cp WebAppCal-*.war s3://project-1-bucket-a/
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