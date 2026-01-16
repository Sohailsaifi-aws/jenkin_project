pipeline {
    agent any

    tools {
        maven 'maven3'
        jdk 'jdk-17'
    }

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESSFUL ✅'
        }
        failure {
            echo 'BUILD FAILED ❌'
        }
    }
}
