pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                npm install
            }
        }

        stage('Start Application') {
            steps {
                npm start
            }
        }

        stage('Run Tests') {
            steps {
                npm test
            }
        }
    }
}
