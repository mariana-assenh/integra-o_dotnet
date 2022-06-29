pipeline{
    agent {
        label 'servidor_plss'
    }
    stages{
        stage('Build'){
            steps{
                script{
                    bat "dotnet restore api1/api1.csproj"
                    bat "dotnet build api1/api1.csproj"        
                }
            }
        }
    }
}
