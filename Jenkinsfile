pipeline {
    agent any

    stages {
        stage('Fetch') {
            steps {
                echo 'Fetching from repo'
                git 'https://github.com/michyre/java-program.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the program'
                bat 'npm install'
                bat 'node hello'
            }
        }
        stage('Execute') {
            steps {
                echo 'Executing...'
                bat 'npm install'
                bat 'node hello'
            }
        }
    }
    post{
        success{
            echo 'Pipeline built successfully'
        }
        failure{
            echo 'Pipeline failed'
        }
    }
}
