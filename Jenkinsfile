stages {
    stage('Build') {
        steps {
            // Commandes pour build Angular
            sh 'cd frontend && npm install && npm run build'

            // Commandes pour build .NET Core
            sh 'cd backend && dotnet build' 
        }
    }
    stage('Test') {
        steps {
            // Commandes pour lancer les tests
            sh 'cd frontend && npm run test' 
            sh 'cd backend && dotnet test' 
        }
    }
    stage('Deploy') {
        steps {
            // Commandes pour deployer l'application
            // ...
        }
    }
}