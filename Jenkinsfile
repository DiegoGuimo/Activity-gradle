pipeline {
    agent any
    tools {
        gradle 'gradle8'  // Asegúrate de que Gradle esté configurado en Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/DiegoGuimo/Activity-gradle.git'
            }
        }
        stage('Build with Gradle') {
            steps {
                script {
                    // Otorgar permisos de ejecución a gradlew
                    sh 'chmod +x ./gradlew'
                    // Construir con Gradle
                    sh './gradlew clean build'
                }
            }
        }
        stage('Test with Gradle') {
            steps {
                script {
                    sh './gradlew test'
                }
            }
        }
    }
}
