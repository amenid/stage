pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Commandes pour build Angular
                sh 'cd ./ui/todo && npm install && npm run build'

                // Commandes pour build .NET Core
                sh 'cd ./api/WebApplication1/WebApplication1 && dotnet build' 
            }
        }
        stage('Test') {
            steps {
                // Commandes pour lancer les tests
                sh 'cd ./ui/todo && npm run test' 
                sh 'cd ./api/WebApplication1/WebApplication1 && dotnet test' 
            }
        }
        stage('Deploy') {
            steps {
                echo 'Nothing to do here yet!'  //  <--  "خطوة"  "فارغة"
            }
        } 
    }
}