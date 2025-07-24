pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                sh '''
                 ls -la
                 node -v
                 npm -version
                 npm ci
                 npm run build
                '''
            }
        }
    }
}
