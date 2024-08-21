// pipeline{
//     agent any
//     stages{
//         stage('Build') {
//             steps {
//                 sh 'echo "hello World" '
//             }
//         }
//     }
// }

pipeline {
    agent any
    stages {
        stage('Build') {
            agent{
                docker{
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                bat '''
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
