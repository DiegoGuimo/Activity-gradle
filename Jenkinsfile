pipeline {
    agent any
    tools {
        maven 'Maven 3.9.9'  // Asegúrate de que Maven esté configurado en Jenkins
        gradle 'Gradle 8.12'  // Asegúrate de que Gradle esté configurado en Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                // Clonar el código del repositorio
                git 'https://github.com/tu_usuario/springboot-pipeline.git'  // Asegúrate de que esta sea la URL correcta de tu repositorio
            }
        }
        stage('Build with Maven') {
            steps {
                script {
                    // Comando para construir el proyecto con Maven
                    sh 'mvn clean install'  // Comando Maven para construir
                }
            }
        }
        stage('Build with Gradle') {
            steps {
                script {
                    // Comando para construir el proyecto con Gradle
                    sh './gradlew clean build'  // Comando Gradle para construir
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Comando para ejecutar las pruebas con Maven
                    sh 'mvn test'  // Comando Maven para ejecutar pruebas
                    
                    // Alternativa con Gradle:
                    sh './gradlew test'  // Comando Gradle para ejecutar pruebas
                }
            }
        }
    }
}
