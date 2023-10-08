pipeline {
    agent any

    stages {
        stage('Récupération du code') {
            steps {
                checkout scm
            }
        }

        stage('Nettoyage et compilation avec Maven') {
            steps {
                sh 'mvn clean compile'
            }
        }
    }

    post {
        success {
            echo 'Le pipeline s\'est terminé avec succès.'
        }
        failure {
            echo 'Le pipeline a échoué.'
        }
    }
}
