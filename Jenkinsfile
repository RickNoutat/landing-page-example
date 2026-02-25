pipeline {
    agent { label 'agent-1' }
    environment {
        AZURE_VM = 'rkydvnci@20.215.208.75'
        IMAGE = 'rickydavinci/landing-page:latest'
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Récupération du code source...'
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Compilation du projet...'
            }
        }
        stage('Test') {
            steps {
                echo 'Exécution des tests...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Déploiement sur Azure...'
                sh """
                    ssh -o StrictHostKeyChecking=no ${AZURE_VM} '
                        docker pull ${IMAGE} &&
                        docker stop landing || true &&
                        docker rm landing || true &&
                        docker run -d --name landing -p 80:80 ${IMAGE}
                    '
                """
            }
        }
    }
}
