pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                script {
                    sh "docker build -f FRONTEND/dockerfile -t ovalencia08/front-crm:latest${BUILD_ID} "
                }
            }
        }
        stage('docker push') {
            steps {
                script {
                    sh "docker push ovalencia08/front-crm:latest${BUILD_ID} "
                }
            }
        }
    }
}