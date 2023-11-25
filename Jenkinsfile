pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Paso para obtener el código del repositorio
                checkout scm
            }
        }
        stage('Install dependencies') {
            steps {
                // Instalar dependencias de React
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                // Compilar la aplicación de React
                sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                // Despliegue de la aplicación en un servidor o en un servicio de hosting
                // Aquí se podría copiar los archivos generados en la etapa de Build a un servidor
                // o subirlos a un servicio como Netlify, Vercel, AWS S3, etc.
                // Ejemplo (puede variar según el entorno):
                sh 'rsync -avz ./build/ user@hostname:/path/to/deploy'
            }
        }
        
    }
}