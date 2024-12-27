pipeline {
    agent any
    tools {
        gradle 'gradle8'  // Asegúrate de que Gradle esté configurado en Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                // Clonar el código del repositorio
                git 'https://github.com/DiegoGuimo/Activity-gradle.git'  // Asegúrate de que esta sea la URL correcta de tu repositorio
            }
        }
        stage('Build with Gradle') {
            steps {
                script {
                    // Construir con Gradle
                    sh './gradlew clean build'
                }
            }
        }
        stage('Test with Gradle') {
            steps {
                script {
                    // Pruebas con Gradle
                    sh './gradlew test'
                }
            }
        }
    }
}
