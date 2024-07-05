pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                git branch: 'main', url: 'git@github.com:amenid/stage.git'
            }
        }
        stage('Build') {
            steps {
                script {
                    // Build Angular
                    dir('frontend') {
                        sh 'ls'
                        sh 'npm install'
                        sh 'npm run build'
                    }
                    // Build .NET Core
                    dir('backend/WebApplication1/WebApplication1') {
                        sh 'dotnet build'
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Test Angular
                    dir('frontend') {
                        sh 'npm run test'
                    }
                    // Test .NET Core
                    dir('backend/WebApplication1/WebApplication1') {
                        sh 'dotnet test'
                    }
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Nothing to do here yet!'  // Placeholder for deployment steps
            }
        }
    }
}
