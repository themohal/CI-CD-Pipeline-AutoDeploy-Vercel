pipeline {
    agent any
    environment {
        // Define any environment variables here
        VERCEL_TOKEN = credentials('vercel-token')
    }
    stages {
        stage('Build') {
            steps {
                // Add build steps here
                bat 'npm install'
                bat 'npm run build'
            }
        }
        stage('Deploy to Vercel') {
            steps {
                // Add deployment steps here
                bat 'npx vercel --prod --yes --token %VERCEL_TOKEN%'
            }
        }
    }
}