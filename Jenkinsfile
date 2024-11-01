pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/yourusername/calculator-project.git'
            }
        }

        stage('Setup and Test') {
            steps {
                // Install dependencies and run tests in one stage
                sh '''
                   pip install -r requirements.txt
                   pytest
                '''
            }
        }

        stage('Build') {
            steps {
                echo 'Build complete!'
            }
        }
    }
}
