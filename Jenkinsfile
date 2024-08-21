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
            steps {
                bat 'echo Hello, World!'  // Use batch command
                // OR
                // powershell 'Write-Host "Hello, World!"'  // Use PowerShell command
            }
        }
    }
}
