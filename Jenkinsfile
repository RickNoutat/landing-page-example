pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: "https://github.com/RickNoutat/landing-page-example"
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
