pipeline {
    agent any

    stages {
                stage('Clean old Artifact') {
            steps {
                sh"""
                rm -rf target
                """
            }
        }
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