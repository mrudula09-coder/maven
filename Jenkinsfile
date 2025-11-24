pipeline {
    agent any

    tools {
        maven 'MAVEN_HOME'
        jdk 'JDK17'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/mrudula09-coder/maven.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }

    post {
        success {
            echo "Build successful!"
        }
        failure {
            echo "Build failed!"
        }
    }
}
