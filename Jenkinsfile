pipeline {
    agent any
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
                echo 'Déploiement en production...'
            }
        }
    }
}

