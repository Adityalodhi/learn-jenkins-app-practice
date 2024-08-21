pipeline {
    agent any
    stages {
        stage('Build') {
            agent{
                docker {
                    image 'node:20.16.0-alpine3.20'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    mkdir -p /.npm && chown -R node:node /.npm
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
