pipeline {
    agent any

    stages {
        stage('bild') {
            agent {
                docker{
                    image 'node:18-alpine'
                    reuseNode tru
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}
