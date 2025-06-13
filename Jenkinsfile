pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }
        stage('Set Up Node.js') {
            steps {
                tool name: 'NodeJS 18', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
            }
        }

        stage('Install Dependencies') {
            steps {
                 sh 'npm install'
            }
        }

        stage('Start Application') {
            steps {
                 sh 'npm start'
            }
        }

        stage('Run Tests') {
            steps {
                 sh 'npm test'
            }
        }
    }
}
