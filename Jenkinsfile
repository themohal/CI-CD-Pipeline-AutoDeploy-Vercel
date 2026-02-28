pipline {
    agent any
    environment {
        // Define any environment variables here
        VERCEL_TOKEN = credentials('vercel-token')
    }
    stages {
        stage('Build') {
            steps {
                // Add build steps here
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Deploy to Vercel') {
            steps {
                // Add deployment steps here
                sh 'npx vercel --token $VERCEL_TOKEN --prod'
            }
        }
    }
}