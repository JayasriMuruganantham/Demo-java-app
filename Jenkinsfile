pipeline {
    agent any

    tools {
        maven 'Maven 3'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/JayasriMuruganantham/Demo-java-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Unit tests ran with build'
            }
        }
    }

    post {
        success {
            echo '✅ Build succeeded!'
        }
        failure {
            echo '❌ Build failed!'
        }
    }
}
