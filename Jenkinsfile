pipeline {
    agent any

    tools {
        maven 'M3'   // Jenkins me 'M3' naam ka Maven tool install hona chahiye
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Debasish-87/hello-java-maven.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
